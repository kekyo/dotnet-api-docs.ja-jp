### <a name="wpf-treeviewitem-must-be-used-within-a-treeview"></a>WPF TreeViewItem をツリー ビュー内で使用する必要があります。

|   |   |
|---|---|
|説明|使用を制限する 4.5 で導入された変更<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>の外部要素、<xref:System.Windows.Controls.TreeView?displayProperty=name>です。 これは、次のような条件で発生します。<ul><li><xref:System.Windows.Controls.TreeViewItem?displayProperty=name>ビジュアル親がパネルではありません。 (A<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>に対して生成された、<xref:System.Windows.Controls.TreeView?displayProperty=name>がその親としてパネル)</li><li><xref:System.Windows.Controls.TreeViewItem?displayProperty=name>の子孫である、<xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name>として機能する、&quot;アイテム ホスト&quot;リスト コントロール (リスト ボックス、データ グリッド、リスト ビューなど)。 仮想化を有効にする必要はありません。</li><li><xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name>項目スクロールは、(<code>ScrollUnit=&quot;Item&quot;</code>)。</li><li>誰かが要素 <code>v</code> をスクロールして表示させるために <code>VirtualizingStackPanel.MakeVisible(v)</code> を呼び出します。 これは、明示的に行うか、さまざまな方法で暗黙的に行うことができます。おそらく、最も一般的な方法は、<code>v</code> をクリックして、キーボードのフォーカスを与えることです。</li><li>ビジュアルの親チェーン<code>v</code>を<xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name>通過、<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>です。</li></ul>つまり、この表示は、ときに、<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>は以外で使用される、<xref:System.Windows.Controls.TreeView?displayProperty=name>の子孫で、ユーザーがクリックして、<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>を表示させます。 場合、<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>子孫のフォーカスを持たない、この問題は表示されません。 これは、ヒット場所状況の例は、ときに、 <xref:System.Windows.Controls.TreeViewItem?displayProperty=name> DataTemplate のルートです。 この問題に遭遇したときには、WPF フレームワーク内で InvalidCastException が発生しています。|
|提案される解決策|このための修正プログラムが使用可能になります。|
|スコープ|マイナー|
|Version|4.5|
|型|ランタイム|

