### <a name="item-scrolling-a-flat-list-with-items-of-different-pixel-height"></a>別のピクセルの高さの項目を含む単純なリストの項目のスクロール

|   |   |
|---|---|
|説明|ときに、<xref:System.Windows.Controls.ItemsControl?displayProperty=name>仮想化を使用して、コレクションが表示されます (<code>IsVirtualizing=true</code>) と項目、スクロール (<code>ScrollUnit=Item</code>)、コントロールはスクロールの高さ (ピクセル単位) は、近隣ノードとは異なる項目を表示するときと、<xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name>すべてを反復処理コレクション内の項目。 この反復処理中には、UI が応答しません。コレクションが大きい場合、ハングとこれに認識されることができます。イテレーションは、以前の .Net リリースにおいても、他の状況で発生します。 たとえばときに、発生ピクセル スクロール (<code>ScrollUnit=Pixel</code>) 項目スクロールする場合は、別のピクセルの高さ、および項目を検出したときに階層データ (など、<xref:System.Windows.Controls.TreeView?displayProperty=name>または<xref:System.Windows.Controls.ItemsControl?displayProperty=name>と有効になっているグループ化) を持つ項目を検出したときに、近隣ノードの子孫の項目の別の数です。項目のスクロールとは異なるピクセルの高さの場合、イテレーションは、階層データのレイアウトでバグを修正するのには、.Net 4.6.1 で導入されました。  データがフラット (階層)、および .Net 4.6.2 されないという点である場合は不要です。|
|提案される解決策|イテレーションが発生した場合、以前のリリースではなく .Net 4.6.1 では場合、<xref:System.Windows.Controls.ItemsControl?displayProperty=name>は項目の単純なリストをスクロールに別のピクセルの高さの項目は、次の 2 つの解決策。<ol><li>.Net 4.6.2 をインストールします。</li><li>.Net 4.6.1 用 HR 1605 の修正プログラムをインストールします。</li></ol>|
|スコープ|マイナー|
|Version|4.6.1|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=nameWithType></li></ul>|

