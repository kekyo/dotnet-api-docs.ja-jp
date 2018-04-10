### <a name="wpf-textbox-selected-text-appears-a-different-color-when-the-text-box-is-inactive"></a>WPF のテキスト ボックスが選択されているテキストでは、テキスト ボックスがアクティブでない場合、それぞれ異なる色が表示されます。

|   |   |
|---|---|
|説明|.NET 4.5 では、WPF テキスト ボックス コントロールがアクティブでないとき (フォーカスがないとき)、ボックス内で選択されているテキストは、コントロールがアクティブなときとは別の色で表示されます。|
|提案される解決策|設定 (.NET 4.0) の以前の動作を復元することがあります、<xref:System.Windows.FrameworkCompatibilityPreferences.AreInactiveSelectionHighlightBrushKeysSupported>プロパティを<code>false</code>です。|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

