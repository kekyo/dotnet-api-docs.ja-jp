### <a name="xslt-style-sheet-exception-message-changed"></a>XSLT スタイル シートの例外のメッセージが変更されました。

|   |   |
|---|---|
|説明|XSLT ファイルが複雑すぎる場合のエラー メッセージのテキストは、.NET Framework 4.5 で&quot;スタイル シートが複雑すぎます。&quot;エラー メッセージが以前のバージョンで&quot;XSLT のコンパイル エラー。&quot;エラー メッセージのテキストに依存するアプリケーション コードは機能しなくなります。 ただし、例外の種類は同じなので、この変更による実質的な影響はありません。|
|提案される解決策|このエラー状態からの例外のメッセージを新しいメッセージを期待できることによって、アプリ コードを更新しますか (さらに良い) 例外の種類にのみ依存するコードを更新 (<xref:System.Xml.Xsl.XsltException?displayProperty=name>)、これは変更されていません。|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Type)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XmlReader)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XPath.IXPathNavigable)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Reflection.MethodInfo,System.Byte[],System.Type[])?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.String,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XmlReader,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XPath.IXPathNavigable,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li></ul>|

