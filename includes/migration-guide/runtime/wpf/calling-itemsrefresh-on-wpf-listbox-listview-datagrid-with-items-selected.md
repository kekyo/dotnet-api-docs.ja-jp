### <a name="calling-itemsrefresh-on-a-wpf-listbox-listview-or-datagrid-with-items-selected-can-cause-duplicate-items-to-appear-in-the-element"></a>WPF のリスト ボックス、ListView、または選択された項目がある DataGrid での通話 Items.Refresh に重複する項目が、要素に表示される可能性があります。

|   |   |
|---|---|
|説明|項目が選択されているときに、コードから ListBox.Items.Refresh を呼び出し、.NET Framework 4.5 で、<xref:System.Windows.Controls.ListBox?displayProperty=name>選択した項目を一覧内で重複する可能性があります。 同様の問題が発生した<xref:System.Windows.Controls.ListView?displayProperty=name>と<xref:System.Windows.Controls.DataGrid?displayProperty=name>です。 これは、.NET Framework 4.6 で修正されます。|
|提案される解決策|この問題をする前に項目をプログラムで解除して回避することがあります<xref:System.Windows.Data.CollectionView.Refresh?displayProperty=name>し再項目を選択、呼び出しが完了した後と呼びます。 または、この問題は .NET Framework 4.6 で修正されたため、このバージョンの .NET Framework にアップグレードすることによって対処できます。|
|スコープ|マイナー|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Windows.Data.CollectionView.Refresh?displayProperty=nameWithType></li></ul>|

