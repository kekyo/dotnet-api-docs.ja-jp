### <a name="wpf-textbox-defaults-to-undo-limit-of-100"></a>WPF の TextBox の既定値は 100 の制限値を元に戻す

|   |   |
|---|---|
|説明|.NET 4.5 では、WPF テキスト ボックスの既定の元に戻す上限は 100 です (.NET 4.0 では無制限でした)。|
|提案される解決策|制限を明示的に設定することができます、元に戻す制限の 100 が低すぎる場合は、 <xref:System.Windows.Controls.Primitives.TextBoxBase.UndoLimit>|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

