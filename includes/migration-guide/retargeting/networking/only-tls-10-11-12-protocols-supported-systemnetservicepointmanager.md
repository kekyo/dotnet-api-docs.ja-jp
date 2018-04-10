### <a name="only-tls-10-11-and-12-protocols-supported-in-systemnetservicepointmanager-and-systemnetsecuritysslstream"></a>System.Net.ServicePointManager および System.Net.Security.SslStream でサポートされている Tls 1.0、1.1 と 1.2 プロトコルのみ

|   |   |
|---|---|
|説明|.NET Framework 4.6 以降で、<xref:System.Net.ServicePointManager>と<xref:System.Net.Security.SslStream>クラスのみを使用できる次の 3 つのプロトコルのいずれかの: Tls1.0、Tls1.1、または Tls1.2 です。 SSL3.0 プロトコルと RC4 の暗号化はサポートされていません。|
|提案される解決策|推奨される軽減策では、サーバー側のアプリを Tls1.0、Tls1.1、または Tls1.2 にアップグレードします。 これが現実的でない場合、またはクライアント アプリが破損している場合は、次の 2 つの方法のいずれかにより、<xref:System.AppContext?displayProperty=name> クラスを使用してこの機能を除外できます。<ol><li>プログラムによって設定 compat スイッチによって、<xref:System.AppContext?displayProperty=name>説明に従って、[ここ](http://blogs.msdn.com/b/dotnet/archive/2015/04/29/net-announcements-at-build-2015.aspx#dotnet46)</li><li>次の行を追加することによって、 <code>&lt;runtime&gt;</code> 、app.config ファイルのセクション:<code>&lt;AppContextSwitchOverrides value=&quot;Switch.System.Net.DontEnableSchUseStrongCrypto=true&quot;/&gt;</code>です。</li></ol>|
|スコープ|マイナー|
|Version|4.6|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Net.SecurityProtocolType.Ssl3?displayProperty=nameWithType></li><li><xref:System.Security.Authentication.SslProtocols.None?displayProperty=nameWithType></li><li><xref:System.Security.Authentication.SslProtocols.Ssl2?displayProperty=nameWithType></li><li><xref:System.Security.Authentication.SslProtocols.Ssl3?displayProperty=nameWithType></li></ul>|

