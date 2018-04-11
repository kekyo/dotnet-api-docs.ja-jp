### <a name="connection-pool-blocking-period-for-azure-sql-databases-is-removed"></a>Azure SQL データベースの期間をブロックして接続プールを削除します。

|   |   |
|---|---|
|説明|以降、.NET Framework 4.6.2 では、接続のオープン要求既知の Azure SQL データベースに (*...database.windows.net を付けて、*. database.chinacloudapi.cn、*. database.usgovcloudapi.net、*. database.cloudapi.de)、ブロックしている期間は、接続プール削除されると、接続の開いているエラーがキャッシュされていないとします。 接続オープン要求の再試行は、一時的な接続エラーのほぼすぐ後に発生します。 この変更により、し、有効になっているクラウド アプリのパフォーマンスを向上させる、Azure SQL データベースに対してすぐに再試行する接続オープン試行します。 他のすべての接続試行中に接続プールのブロック期間は適用するのには続行されます。 .NET Framework 4.6.1 以前のバージョンで、アプリでは、データベースに接続するときに一時的な接続エラーが発生したときに、接続試行を再試行できません早すぎると、接続プールが、エラーをキャッシュし、1 を 5 秒間に再スローされます。1 分です。 詳細については、次を参照してください。 [SQL サーバー接続プール (ADO.NET)](~/docs/framework/data/adonet/sql-server-connection-pooling.md)です。 この動作は、Azure SQL データベースへの接続時に問題となります。多くの場合、一時的なエラーが発生し、通常数秒内に回復します。 接続プールのブロック機能は、アプリに接続できないこと、データベースが広範囲にわたって、場合でも、データベースが使用され、数秒以内に表示するために、アプリが必要なを意味します。|
|提案される解決策|接続プールのブロッキング期間を設定して構成できますこの動作が望ましくない場合、<xref:System.Data.SqlClient.SqlConnectionStringBuilder.PoolBlockingPeriod?displayProperty=name>プロパティは、.NET Framework 4.6.2 で導入されました。 プロパティ値が <xref:System.Data.SqlClient.PoolBlockingPeriod?displayProperty=name> 列挙型のメンバーである場合、次の 3 つの値のいずれかを使用できます。<ul><li><xref:System.Data.SqlClient.PoolBlockingPeriod.AlwaysBlock></li><li><xref:System.Data.SqlClient.PoolBlockingPeriod.Auto></li><li><xref:System.Data.SqlClient.PoolBlockingPeriod.NeverBlock></li></ul><xref:System.Data.SqlClient.SqlConnectionStringBuilder.PoolBlockingPeriod?displayProperty=name> プロパティを <xref:System.Data.SqlClient.PoolBlockingPeriod.AlwaysBlock> に設定して、以前の動作を復元することができます。|
|スコープ|マイナー|
|Version|4.6.2|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Data.Common.DbConnection.OpenAsync?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.Open?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.OpenAsync(System.Threading.CancellationToken)?displayProperty=nameWithType></li></ul>|

