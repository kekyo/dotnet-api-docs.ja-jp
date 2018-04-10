### <a name="xmlschemaexception-now-sets-line-positions-properly"></a>XmlSchemaException 行位置を正しく設定ようになりました

|   |   |
|---|---|
|説明|場合、<xref:System.Xml.Linq.LoadOptions.SetLineInfo>ロード メソッドに値が渡され、検証エラーが発生した、<xref:System.Xml.Schema.XmlSchemaException.LineNumber>と<xref:System.Xml.Schema.XmlSchemaException.LinePosition>プロパティに行情報が含まれています。|
|提案される解決策|例外処理コードに与えられている<xref:System.Xml.Schema.XmlSchemaException.LineNumber>と<xref:System.Xml.Schema.XmlSchemaException.LinePosition>されませんセットは、これらのプロパティはここで設定されるため正しく SetLineInfo を XML の読み込み中に使用する場合、更新する必要があります。|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Xml.Linq.LoadOptions.SetLineInfo?displayProperty=nameWithType></li></ul>|

