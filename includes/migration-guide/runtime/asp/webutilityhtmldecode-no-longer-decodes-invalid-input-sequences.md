### <a name="webutilityhtmldecode-no-longer-decodes-invalid-input-sequences"></a>WebUtility.HtmlDecode が不要になったに無効な入力シーケンスをデコードします。

|   |   |
|---|---|
|説明|既定では、デコード メソッドによって無効な入力シーケンスが無効な UTF-16 文字列にデコードされることがなくなりました。 代わりに、元の入力が返されます。|
|提案される解決策|デコーダーの出力の変更は、UTF-16 データではなくバイナリ データを文字列に格納した場合にのみ影響があります。 この動作を明示的に制御するには、次のように設定します。、<code>aspnet:AllowRelaxedUnicodeDecoding</code>の属性、 [appSettings](~/docs/framework/configure-apps/file-schema/appsettings/index.md)要素<code>true</code>レガシの動作を有効にまたは<code>false</code>を現在の動作を有効にします。|
|スコープ|マイナー|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Net.WebUtility.HtmlDecode(System.String)?displayProperty=nameWithType></li><li><xref:System.Net.WebUtility.HtmlDecode(System.String,System.IO.TextWriter)?displayProperty=nameWithType></li><li><xref:System.Net.WebUtility.UrlDecode(System.String)?displayProperty=nameWithType></li></ul>|

