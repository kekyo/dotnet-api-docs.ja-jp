### <a name="scrolling-a-wpf-treeview-or-grouped-listbox-in-a-virtualizingstackpanel-can-cause-a-hang"></a>WPF TreeView コントロールまたは、VirtualizingStackPanel でグループ化されたボックスの一覧をスクロールすると、ハング可能性があります。

|   |   |
|---|---|
|説明|.NET Framework v4.5 でスクロール WPF<xref:System.Windows.Controls.TreeView?displayProperty=name>仮想化スタック パネルと、ハング、ビューポートの余白がある場合 (内の項目間、 <xref:System.Windows.Controls.TreeView?displayProperty=name>ItemsPresenter 要素で、やなど)。 さらに、場合によっては、ビュー内にサイズの異なる項目があると、余白がない場合でも、不安定になることがあります。|
|提案される解決策|このバグは、.NET Framework 4.5.1 にアップグレードすることによって回避できます。 余白をビューのコレクションから削除する代わりに、(と同様に<xref:System.Windows.Controls.TreeView?displayProperty=name>s) 内での仮想化スタック パネルすべての項目が含まれている場合は、同じサイズです。|
|スコープ|Major|
|バージョン|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Windows.Controls.VirtualizingStackPanel.SetIsVirtualizing(System.Windows.DependencyObject,System.Boolean)?displayProperty=nameWithType></li></ul>|

