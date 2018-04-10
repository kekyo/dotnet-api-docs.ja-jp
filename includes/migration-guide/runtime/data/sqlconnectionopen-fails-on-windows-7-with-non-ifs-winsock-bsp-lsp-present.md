### <a name="sqlconnectionopen-fails-on-windows-7-with-non-ifs-winsock-bsp-or-lsp-present"></a>非 IFS Winsock BSP または LSP 存在で Windows 7 で SqlConnection.Open が失敗します。

|   |   |
|---|---|
|説明|<xref:System.Data.SqlClient.SqlConnection.Open> および<xref:System.Data.SqlClient.SqlConnection.OpenAsync(System.Threading.CancellationToken)>IFS Winsock BSP ではない LSP と Windows 7 コンピューターで実行されているが、コンピューターに存在する場合は、.NET Framework 4.5 で失敗します。IFS BSP 以外または LSP がインストールされているかどうかを判断するのには、使用、<code>netsh WinSock Show Catalog</code>コマンドを使用し、確認すべて<code>Winsock Catalog Provider Entry</code>返される項目。 Service Flags 値の <code>0x20000</code> ビットがセットされている場合、プロバイダーは IFS ハンドルを使用していて、正しく機能します。 <code>0x20000</code> ビットがクリアされている (セットされていない) 場合は、IFS 以外の BSP または LSP です。|
|提案される解決策|このバグは .NET framework 4.5.2 で修正されたため、.NET Framework をアップグレードすることによって回避できます。 または、インストールされている IFS 以外の Winsock LSP を削除することによって回避できます。|
|スコープ|マイナー|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Data.SqlClient.SqlConnection.Open?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.OpenAsync(System.Threading.CancellationToken)?displayProperty=nameWithType></li></ul>|

