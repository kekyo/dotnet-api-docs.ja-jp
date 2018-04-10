### <a name="itemsclear-does-not-remove-duplicates-from-selecteditems"></a>Items.Clear は、SelectedItems から重複部分は削除されません。

|   |   |
|---|---|
|説明|(複数選択が有効になっている) のセレクターに重複があるとすると、<xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>コレクションに同じアイテムが複数回出現します。  それらを削除に失敗した (例: を Items.Clear を呼び出して) のデータ ソースからこれらの項目を削除する<xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>だけ最初のインスタンスを削除します。 さらの後で使用<xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>(例: SelectedItems.Clear()) が発生する問題など<xref:System.ArgumentException?displayProperty=name>ので、<xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>不要になったデータ ソース内にあるアイテムが含まれています。|
|提案される解決策|.NET 4.6.2 可能であればアップグレードします。|
|スコープ|マイナー|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=nameWithType></li></ul>|

