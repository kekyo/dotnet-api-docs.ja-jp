### <a name="wcf-binding-with-the-transportwithmessagecredential-security-mode"></a>TransportWithMessageCredential セキュリティ モードでの WCF バインド

|   |   |
|---|---|
|説明|以降、.NET Framework 4.6.1 では、TransportWithMessageCredential セキュリティ モードを使用する WCF バインドを設定できます符号なしでメッセージを受信する&quot;に&quot;非対称セキュリティ キーのヘッダー。既定では、署名されていない&quot;に&quot;.NET 4.6.1 で拒否されるヘッダーが続行されます。 これらはのみ受け付けられます Switch.System.ServiceModel.AllowUnsignedToHeader 構成スイッチを使用して操作のこの新しいモードにアプリケーションを選んだ場合。これはオプトイン機能であるために、既存のアプリの動作に影響はありません。|
|提案される解決策|これはオプトイン機能であるため、既存のアプリの動作に影響はないはずです。 新しい動作を使用するかどうかを制御するには、次の構成設定を使用します。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.AllowUnsignedToHeader=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|スコープ|透明|
|Version|4.6.1|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.ServiceModel.BasicHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.BasicHttpsSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.WSFederationHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li></ul>|

