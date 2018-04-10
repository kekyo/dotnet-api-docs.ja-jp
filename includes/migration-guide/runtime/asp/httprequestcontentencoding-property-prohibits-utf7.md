### <a name="httprequestcontentencoding-property-prohibits-utf7"></a>HttpRequest.ContentEncoding プロパティには、UTF7 が禁止されています

|   |   |
|---|---|
|説明|.NET Framework 4.5 以降、utf-7 エンコードは禁止されていますで<xref:System.Web.HttpRequest?displayProperty=name>s' 本文。 UTF-7 データの受信を必要とするアプリケーションのデータが、正しくデコードされない場合があります。|
|提案される解決策|Utf-7 でのエンコードを使用しないようにアプリケーションを更新することをお勧め<xref:System.Web.HttpRequest?displayProperty=name>s。 または、[<appSettings>](https://msdn.microsoft.com/library/hh975440(v=vs.110).aspx) 要素の <code>aspnet:AllowUtf7RequestContentEncoding</code> 属性を使用して、レガシ動作に戻すことができます。|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Web.HttpRequest.ContentEncoding?displayProperty=nameWithType></li></ul>|

