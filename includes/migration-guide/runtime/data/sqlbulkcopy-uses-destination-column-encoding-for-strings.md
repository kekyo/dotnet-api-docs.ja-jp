### <a name="sqlbulkcopy-uses-destination-column-encoding-for-strings"></a>文字列の変換先列のエンコード SqlBulkCopy を使用してください。

|   |   |
|---|---|
|説明|データを列に挿入する場合、<xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> は <code>VARCHAR</code> と <code>CHAR</code> の型の既定エンコードではなく、挿入先の列のエンコードを使用します。 この変更により、挿入先の列が既定のエンコードを使用しない場合に、既定のエンコードを使用することによって発生するデータ破損の可能性がなくなります。 まれに、エンコードの変更が大きすぎて、変換先列に収まるようにデータを生成した場合、既存のアプリケーションによって SqlException 例外がスローする可能性があります。|
|提案される解決策|期待<xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name>の相違点をエンコードするためのデータが破損不要になった。 変換先列のサイズの上限に近づいて文字列がコピーされている場合がありますか、事前 (コピーするデータを変換先列のデータが収まることを確認する) をエンコードするために必要なまたはキャッチ<xref:System.Data.SqlClient.SqlException?displayProperty=name>s。|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlBulkCopy.%23ctor(System.Data.SqlClient.SqlConnection)?displayProperty=nameWithType></li></ul>|

