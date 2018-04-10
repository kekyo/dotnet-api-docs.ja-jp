### <a name="datagridcellspanelbringindexintoview-throws-argumentoutofrangeexception"></a>DataGridCellsPanel.BringIndexIntoView ArgumentOutOfRangeException をスローします。

|   |   |
|---|---|
|説明|<xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)> 非同期的に列の仮想化が有効になっているが、列の幅がまだ決定されていません。  非同期の作業が発生する前に、列が削除された場合、<xref:System.ArgumentOutOfRangeException?displayProperty=name>発生することができます。|
|提案される解決策|次のいずれかの:<ol><li>.NET 4.7 にアップグレードします。</li><li>.NET 4.6.2 用の最新のサービスの修正プログラムをインストールします。</li><li>非同期応答するまでの列が削除されないように<xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)>が完了しました。</li></ol>|
|スコープ|エッジ|
|Version|4.6.2|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object,System.Windows.Controls.DataGridColumn)?displayProperty=nameWithType></li></ul>|

