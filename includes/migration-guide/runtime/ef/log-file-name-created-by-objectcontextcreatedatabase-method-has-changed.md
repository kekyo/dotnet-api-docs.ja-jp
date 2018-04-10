### <a name="log-file-name-created-by-the-objectcontextcreatedatabase-method-has-changed-to-match-sql-server-specifications"></a>SQL Server の仕様に合わせて ObjectContext.CreateDatabase メソッドによって作成されたログ ファイルの名前が変更されました。

|   |   |
|---|---|
|説明|ときに、<xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=name>メソッドを直接呼び出してまたは SqlClient プロバイダーと接続文字列で AttachDBFilename 値で Code First を使用して (ファイル名は、name のコマンドを実行しではなく filename_log.ldf をというログ ファイルを作成指定されたファイル AttachDBFilename 値)。 この変更により、SQL Server の仕様に従ってログ ファイル名が提供されるため、デバッグ機能が向上します。|
|提案される解決策|ログ ファイル名がアプリケーションにとって重要な場合、標準の _log.ldf ファイル名形式を予期するように、アプリケーションを更新する必要があります。|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=nameWithType></li></ul>|

