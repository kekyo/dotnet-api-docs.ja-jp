### <a name="mef-catalogs-implement-ienumerable-and-therefore-can-no-longer-be-used-to-create-a-serializer"></a>MEF カタログ IEnumerable が実装され、そのため、シリアライザーを作成することができます使用されなく

|   |   |
|---|---|
|説明|以降、.NET Framework 4.5 では、MEF カタログで IEnumerable を実装し、そのため、シリアライザーを作成することが使用されなく (<xref:System.Xml.Serialization.XmlSerializer?displayProperty=name>オブジェクト)。 MEF カタログをシリアル化しようとすると、例外がスローされます。|
|提案される解決策|シリアライザーの作成に MEF を使用できなくなりました。|
|スコープ|Major|
|バージョン|4.5|
|型|ランタイム|

