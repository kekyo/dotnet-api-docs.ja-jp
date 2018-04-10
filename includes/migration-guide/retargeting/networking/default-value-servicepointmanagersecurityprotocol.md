### <a name="default-value-of-servicepointmanagersecurityprotocol-is-securityprotocoltypesystemdefault"></a>ServicePointManager.SecurityProtocol の既定値は SecurityProtocolType.System.Default

|   |   |
|---|---|
|説明|.NET Framework 4.7 の既定値を対象とするアプリで始まる、<xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType>プロパティは<xref:System.Net.SecurityProtocolType.SystemDefault?displayProperty=nameWithType>します。 この変更により、.NET Framework SslStream (FTP、HTTPS、および SMTP) など、.NET Framework で定義されているハード コーディングされた値を使用する代わりに、オペレーティング システムから既定のセキュリティ プロトコルを継承するに基づいてネットワーク Api です。 既定値は、オペレーティング システムと、システム管理者によって実行される任意のカスタム構成によって異なります。 詳細については、Windows オペレーティング システムの各バージョンで既定の SChannel プロトコルは、次を参照してください。 [TLS/SSL (Schannel SSP) のプロトコル](https://msdn.microsoft.com/library/windows/desktop/mt808159.aspx)です。既定値である .NET Framework の以前のバージョンを対象とするアプリケーションの<xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType>プロパティは、対象とする .NET Framework のバージョンによって異なります。 参照してください、 [.NET Framework 4.5.2 に 4.6 からの移行の変更の再ターゲットのネットワー キング セクション](~/docs/framework/migration-guide/retargeting/4.5.2-4.6.md#networking)詳細についてはします。|
|提案される解決策|この変更では、.NET Framework 4.7 またはそれ以降のバージョンを対象とするアプリケーションに影響します。システムの既定の証明書利用者は、明示的に設定できますの値よりも定義されているプロトコルを使用する場合、<xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType>プロパティです。この変更が望ましくない場合は、選択を解除する、構成設定を追加して、 [\<ランタイム >](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)アプリケーション構成ファイルのセクションです。 次の例はどちらも、<code>&lt;runtime&gt;</code>セクションおよび<code>Switch.System.Net.DontEnableSystemDefaultTlsVersions</code>オプトアウト スイッチ。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Net.DontEnableSystemDefaultTlsVersions=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|スコープ|マイナー|
|Version|4.7|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType></li></ul>|

