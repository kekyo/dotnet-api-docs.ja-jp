### <a name="wcf-message-security-now-is-able-to-use-tls11-and-tls12"></a>WCF メッセージ セキュリティは今すぐ TLS1.1 と TLS1.2 を使用することが

|   |   |
|---|---|
|説明|.NET Framework 4.7 以降、顧客、または構成できます TLS1.1 TLS1.2 SSL3.0 と TLS1.0 に加えてアプリケーション構成の設定での WCF メッセージ セキュリティにします。|
|提案される解決策|.NET Framework 4.7 に WCF メッセージ セキュリティに TLS1.1 と TLS1.2 をサポートは既定では無効です。 次の行を追加することで有効にすることができます、 <code>&lt;runtime&gt;</code> app.config または web.config ファイルのセクション。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableUsingServicePointManagerSecurityProtocols=false;Switch.System.Net.DontEnableSchUseStrongCrypto=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|スコープ|エッジ|
|Version|4.7|
|型|再ターゲット中|

