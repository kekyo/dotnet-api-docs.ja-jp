### <a name="tls-1x-by-default-passes-the-schsendauxrecord-flag-to-the-underlying-schannel-api"></a>TLS 1.x 既定では、基になる SCHANNEL API を SCH_SEND_AUX_RECORD フラグを渡します

|   |   |
|---|---|
|説明|TLS を使用するときに 1.x では、.NET Framework は、基になる Windows SCHANNEL API に依存しています。 .NET Framework 4.6 以降、 [SCH_SEND_AUX_RECORD](https://msdn.microsoft.com/library/windows/desktop/aa379810.aspx) SCHANNEL にフラグが既定で渡されます。 これにより、個別の 2 つのレコード、1 バイトと 2 番目として最初に暗号化されるデータを分割する SCHANNEL <em>n</em>-1 バイトまでです。まれなケースでは、クライアントとデータが 1 つのレコードに格納されている想定を行う既存のサーバー間の通信を停止します。|
|提案される解決策|この変更は、既存のサーバーとの通信を中断、無効にできますを送信する、 [SCH_SEND_AUX_RECORD](https://msdn.microsoft.com/library/windows/desktop/aa379810.aspx)フラグし、を次のスイッチを追加することで、別のレコードにデータを分割しないの以前の動作を復元します[ \<AppContextSwitchOverrides >](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md)で、 [ ` ](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)アプリ構成ファイル。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Net.DontEnableSchSendAuxRecord=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre> <blockquote> [!IMPORTANT] この設定は、旧バージョンと互換性のためだけに提供されます。 使用はそれ以外の場合推奨されていません。</blockquote> |
|スコープ|エッジ|
|Version|4.6|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Net.Security.SslStream?displayProperty=nameWithType></li><li><xref:System.Net.ServicePointManager?displayProperty=nameWithType></li><li><xref:System.Net.Http.HttpClient?displayProperty=nameWithType></li><li><xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType></li><li><xref:System.Net.HttpWebRequest?displayProperty=nameWithType></li><li><xref:System.Net.FtpWebRequest?displayProperty=nameWithType></li></ul>|

