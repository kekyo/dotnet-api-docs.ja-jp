### <a name="flowdocument-may-show-an-extra-line-of-text"></a>FlowDocument は余分な行のテキストを表示することがあります。

|   |   |
|---|---|
|説明|場合によっては、<xref:System.Windows.Documents.FlowDocument>要素は、.NET Framework 4.0 で実行時の表示と比較して、.NET Framework 4.5 で実行されているときに余分な行のテキストに表示されます。 以前から除外されたに表示されるテキストことが原因で、表示されるテキストをほとんど、または明る、変更の既知のケースがない可能性が、 <xref:System.Windows.Documents.FlowDocument>'s を表示します。|
|提案される解決策|場合によっては、いずれかで表示要素の PageHeight プロパティを小さく表示されている行の前の番号を復元できます。|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Windows.Documents.FlowDocument.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Documents.FlowDocument.%23ctor(System.Windows.Documents.Block)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentReader.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentPageViewer.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.DocumentPageView.%23ctor?displayProperty=nameWithType></li></ul>|

