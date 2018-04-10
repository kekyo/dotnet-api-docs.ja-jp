### <a name="wpf-spell-checking-fails-in-unexpected-ways"></a>予期しない方法で WPF スペル チェックが失敗します。

|   |   |
|---|---|
|説明|これには、WPF スペル チェック機能の問題の数が含まれます。<ul><li>WPF のスペル チェック機能が場合がありますがスローされます。 <xref:System.Runtime.InteropServices.COMException?displayProperty=name></li><li>WPF スペル チェックが失敗し<xref:System.UnauthorizedAccessException>'別のユーザーとして実行 を使用してアプリケーションが起動されたときに</li><li>WPF のスペル チェック機能がドイツ語で 'Hausnummer' のような複合語でスペル ミスを正しく識別します。</li></ul>|
|提案される解決策|問題 1 - これは .NET Framework 4.6.2 で修正されました '別のユーザーとして実行 を使用してアプリケーションが起動されたときに、問題 2 - WPF スペル チェック機能がサポートされていません。 .NET Framework 4.6.2 以降では、この方法で起動するアプリケーションが予期せずにクラッシュ不要になった-、代わりに、スペル チェック機能が自動的に無効になります。 問題 3 - これは .NET Framework 4.6.2 で修正されました。|
|スコープ|エッジ|
|Version|4.6.1|
|型|ランタイム|

