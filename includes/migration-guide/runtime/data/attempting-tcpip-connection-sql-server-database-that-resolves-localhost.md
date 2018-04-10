### <a name="attempting-a-tcpip-connection-to-a-sql-server-database-that-resolves-to-localhost-fails"></a>解決される SQL Server データベースへの TCP/IP 接続を試みる`localhost`が失敗します。

|   |   |
|---|---|
|説明|.NET Framework 4.6 および 4.6.1 でに解決される SQL Server データベースへの TCP/IP 接続しようとしています。<code>localhost</code>はエラーで失敗&quot;SQL Server への接続を確立中にネットワーク関連またはインスタンス固有のエラーが発生しました。 サーバーが見つからないかアクセスできません。 インスタンス名が正しいこと、および SQL Server がリモート接続を許可するように構成されていることを確認してください。 (プロバイダー: SQL Network Interfaces、エラー: 26 - エラーの検索のサーバー/インスタンスの指定)&quot;|
|提案される解決策|この問題が解消され、以前の動作は、.NET Framework 4.6.2 で復元します。 解決される SQL Server databsae への接続に<code>localhost</code>、.NET Framework 4.6.2 にアップグレードします。|
|スコープ|マイナー|
|Version|4.6|
|型|ランタイム|

