### <a name="adonet-now-attempts-to-automatically-reconnect-broken-sql-connections"></a>ADO.NET は、今すぐ SQL 接続が切断されたを自動的に再接続を試みます

|   |   |
|---|---|
|説明|.NET framework 4.5.1 以降では、.NET Framework は SQL 接続が切断されたを自動的に再接続を試みます。 これは通常のアプリの信頼性を高める、ことを知っておくアプリが必要なエッジ ケースがあるが再接続したときに何らかのアクションがかかることができるように、接続が失われました。|
|提案される解決策|この機能が互換性の問題により望ましくない場合に無効にできる設定して、<xref:System.Data.SqlClient.SqlConnectionStringBuilder.ConnectRetryCount?displayProperty=name>接続文字列のプロパティ (または<xref:System.Data.SqlClient.SqlConnectionStringBuilder?displayProperty=name>) を 0 にします。|
|スコープ|エッジ|
|Version|4.5.1|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Data.IDbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Configuration.ConnectionStringSettings.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor(System.Boolean)?displayProperty=nameWithType></li></ul>|

