### <a name="intermittently-unable-to-scroll-to-bottom-item-in-itemscontrols-like-listbox-and-datagrid-when-using-custom-datatemplates"></a>ItemsControls (リスト ボックスやデータ グリッド) などの項目を下にスクロールする断続的にできませんカスタム Datatemplate を使用する場合。

|   |   |
|---|---|
|説明|場合によっては、.NET Framework 4.5 でのバグの ItemsControls 原因は (のような<xref:System.Windows.Controls.ListBox?displayProperty=name>、 <xref:System.Windows.Controls.ComboBox?displayProperty=name>、<xref:System.Windows.Controls.DataGrid?displayProperty=name>など) カスタム Datatemplate を使用する場合、最下位の項目をスクロールします。 (上へスクロールした後で) もう一度スクロールを試みると、今度はスクロールできます。|
|提案される解決策|この問題は .NET Framework 4.5.2 で修正されたため、このバージョン (またはそれ以降のバージョン) の .NET Framework にアップグレードすることによって対処できます。 または、ユーザーは、スクロール バーをこれらのコレクションの最後の項目までドラッグできますが、2 回試みなければならないことがあります。|
|スコープ|マイナー|
|Version|4.5|
|型|ランタイム|

