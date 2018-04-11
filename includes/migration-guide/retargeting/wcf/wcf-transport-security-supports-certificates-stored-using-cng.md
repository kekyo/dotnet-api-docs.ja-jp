### <a name="wcf-transport-security-supports-certificates-stored-using-cng"></a>WCF トランスポート セキュリティは、CNG を使用して格納されている証明書をサポートしています。

|   |   |
|---|---|
|説明|以降をターゲットとする .NET Framework 4.6.2 アプリでは、WCF トランスポート セキュリティは、Windows 暗号化ライブラリ (CNG) を使用して格納されている証明書をサポートします。 このサポートは、指数の長さが 32 ビット以下の公開キーを持つ証明書に限定されます。 アプリケーションが対象 .NET Framework 4.6.2、ときにこの機能は既定でオンです。 .NET Framework の以前のバージョンで X509 を使用しようとすると、証明書を CSG のキー記憶域プロバイダーが例外をスローします。|
|提案される解決策|ターゲット .NET Framework 4.6.1 と以前のですが、.NET Framework 4.6.2 で実行されているアプリは、次の行を追加することで CNG 証明書のサポートを有効にできます、 <code>&lt;runtime&gt;</code> app.config または web.config ファイルのセクション。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableCngCertificates=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>次のコードを使用してプログラムで行うこともできます。<pre><code class="language-cs">private const string DisableCngCertificates = @&quot;Switch.System.ServiceModel.DisableCngCertificate&quot;;&#13;&#10;AppContext.SetSwitch(disableCngCertificates, false);&#13;&#10;</code></pre><pre><code class="language-vb">Const DisableCngCertificates As String = &quot;Switch.System.ServiceModel.DisableCngCertificates&quot;&#13;&#10;AppContext.SetSwitch(disableCngCertificates, False)&#13;&#10;</code></pre>この変更のため、CNG 証明書の失敗で、セキュリティで保護された通信を開始する試行に依存する例外処理コードは、実行されなくなることに注意してください。|
|スコープ|マイナー|
|Version|4.6.2|
|型|再ターゲット中|

