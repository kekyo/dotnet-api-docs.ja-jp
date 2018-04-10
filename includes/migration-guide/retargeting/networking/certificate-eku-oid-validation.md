### <a name="certificate-eku-oid-validation"></a>証明書の EKU OID の検証

|   |   |
|---|---|
|説明|.NET Framework 4.6 以降、<xref:System.Net.Security.SslStream>または<xref:System.Net.ServicePointManager>クラスが強化されたキーの使用 (EKU) のオブジェクト識別子 (OID) の検証を実行します。 拡張キー使用法 (EKU) 拡張機能とは、キーを使用するアプリケーションを示すオブジェクト識別子 (Oid) のコレクション。 EKU OID の検証は、リモート証明書が本来の目的の正しい Oid を持つようにするためリモート証明書のコールバックを使用します。|
|提案される解決策|次のスイッチに追加することで証明書の EKU OID の検証を無効にできますこの変更が望ましくない場合、 [ \<AppContextSwitchOverrides >](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md)で、 [ ` ](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)のアプリ構成ファイル:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Net.DontCheckCertificateEKUs=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre> <blockquote> [!IMPORTANT] この設定は、旧バージョンと互換性のためだけに提供されます。 使用はそれ以外の場合推奨されていません。</blockquote> |
|スコープ|マイナー|
|Version|4.6|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Net.Security.SslStream?displayProperty=nameWithType></li><li><xref:System.Net.ServicePointManager?displayProperty=nameWithType></li><li><xref:System.Net.Http.HttpClient?displayProperty=nameWithType></li><li><xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType></li><li><xref:System.Net.HttpWebRequest?displayProperty=nameWithType></li><li><xref:System.Net.FtpWebRequest?displayProperty=nameWithType></li></ul>|

