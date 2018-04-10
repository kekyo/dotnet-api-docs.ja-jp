### <a name="listboxitem-isselected-binding-issue-with-observablecollectionlttgtmove"></a>ListBoxItem が選択されているバインド問題 ObservableCollection&lt;T&gt;です。移動

|   |   |
|---|---|
|説明|呼び出す<xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)>または<xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)>にバインドされているコレクションに対して、<xref:System.Windows.Controls.ListBox?displayProperty=name>選択項目を含むの将来の選択またはの unselection、不適切な動作につながる<xref:System.Windows.Controls.ListBox?displayProperty=name>項目。|
|提案される解決策|呼び出す<xref:System.Collections.ObjectModel.Collection%601.Remove(%600)?displayProperty=name>と<xref:System.Collections.ObjectModel.Collection%601.Insert(System.Int32,%600)?displayProperty=name>の代わりに<xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)>この問題を回避します。 または、この問題は .NET Framework 4.6 で修正されたため、このバージョンの .NET Framework にアップグレードすることによって対処できます。|
|スコープ|マイナー|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)?displayProperty=nameWithType></li><li><xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)?displayProperty=nameWithType></li></ul>|

