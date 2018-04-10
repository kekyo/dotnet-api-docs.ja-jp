### <a name="calling-datagridcommitedit-from-a-celleditending-handler-drops-focus"></a>フォーカスをドロップ CellEditEnding ハンドラーから DataGrid.CommitEdit を呼び出す

|   |   |
|---|---|
|説明|呼び出す<xref:System.Windows.Controls.DataGrid.CommitEdit>のいずれかから、<xref:System.Windows.Controls.DataGrid?displayProperty=name>の<xref:System.Windows.Controls.DataGrid.CellEditEnding?displayProperty=name>イベント ハンドラーにより、<xref:System.Windows.Controls.DataGrid?displayProperty=name>フォーカスが失われる。|
|提案される解決策|このバグは .NET framework 4.5.2 で修正されたため、.NET Framework をアップグレードすることによって回避できます。 代わりに、できる限りを明示的に再選択すると、<xref:System.Windows.Controls.DataGrid?displayProperty=name>呼び出した後<xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=name>です。|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.CommitEdit(System.Windows.Controls.DataGridEditingUnit,System.Boolean)?displayProperty=nameWithType></li></ul>|

