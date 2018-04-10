### <a name="accessing-a-wpf-datagrids-selected-items-from-a-handler-of-the-datagrids-unloadingrow-event-can-cause-a-nullreferenceexception"></a>DataGrid の UnloadingRow イベントのハンドラーから WPF DataGrid の選択した項目をアクセスすると、NullReferenceException が発生することができます。

|   |   |
|---|---|
|説明|.NET Framework 4.5 用のイベント ハンドラーのバグにより<xref:System.Windows.Controls.DataGrid>行の削除に関連するイベントが発生した、<xref:System.NullReferenceException?displayProperty=name>にアクセスする場合にスローされる、<xref:System.Windows.Controls.DataGrid>の<xref:System.Windows.Controls.Primitives.Selector.SelectedItem?displayProperty=name>または<xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>プロパティです。|
|提案される解決策|この問題は、.NET Framework 4.6 で修正されており、.NET Framework のバージョンにアップグレードすることで対処することがあります。|
|スコープ|マイナー|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Windows.Controls.DataGrid.UnloadingRow?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.UnloadingRowDetails?displayProperty=nameWithType></li></ul>|

