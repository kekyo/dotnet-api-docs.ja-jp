### <a name="different-exception-handling-for-objectcontextcreatedatabase-and-dbproviderservicescreatedatabase-methods"></a>別の例外処理の ObjectContext.CreateDatabase および DbProviderServices.CreateDatabase メソッド

|   |   |
|---|---|
|説明|.NET 4.5 から、データベースの作成が失敗した場合、<code>CreateDatabase</code> メソッドは、空のデータベースの削除を試みます。 その操作が成功した場合、元の <xref:System.Data.SqlClient.SqlException?displayProperty=name> は伝播されます (.NET 4.0 で常にスローされていた <xref:System.InvalidOperationException?displayProperty=name> の代わりに)。|
|提案される解決策|キャッチすると、<xref:System.InvalidOperationException?displayProperty=name>の実行中に<xref:System.Data.Objects.ObjectContext.CreateDatabase>または<xref:System.Data.Common.DbProviderServices.CreateDatabase(System.Data.Common.DbConnection,System.Nullable{System.Int32},System.Data.Metadata.Edm.StoreItemCollection)>SQLExceptions もキャッチされるようになりました。|
|スコープ|マイナー|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbProviderServices.CreateDatabase(System.Data.Common.DbConnection,System.Nullable{System.Int32},System.Data.Metadata.Edm.StoreItemCollection)?displayProperty=nameWithType></li></ul>|

