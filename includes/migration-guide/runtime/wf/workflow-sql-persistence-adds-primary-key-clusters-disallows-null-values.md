### <a name="workflow-sql-persistence-adds-primary-key-clusters-and-disallows-null-values-in-some-columns"></a>ワークフローの SQL 永続化を追加主キーがクラスターし、一部の列に null 値は許可されていません

|   |   |
|---|---|
|説明|.NET Framework 4.7 から始めて、SqlWorkflowInstanceStoreSchema.sql スクリプトによって SQL ワークフロー インスタンス ストア (SWIS) 用に作成されたテーブルはクラスター化された主キーを使用します。 このため、ユーザーはサポートしていない<code>null</code>値。 SWIS の操作は、この変更による影響はありません。 更新プログラムが SQL Server のトランザクション レプリケーションをサポートするために行われました。|
|提案される解決策|SqlWorkflowInstanceStoreSchemaUpgrade.sql SQL ファイルは、この変更が発生するために、既存のインストールに適用する必要があります。 新しいデータベースのインストールは、変更を自動的にがあります。|
|スコープ|エッジ|
|Version|4.7|
|型|ランタイム|

