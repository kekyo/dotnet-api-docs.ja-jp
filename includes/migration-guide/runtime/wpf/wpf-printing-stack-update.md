### <a name="wpf-printing-stack-update"></a>WPF 印刷スタック更新プログラム

|   |   |
|---|---|
|説明|WPF の印刷 Api を使用して<xref:System.Printing.PrintQueue?displayProperty=name>ウィンドウの印刷ドキュメント パッケージ API の代わりに、現在は非推奨の XPS 印刷 API を呼び出すようになりました。 変更されたと保守性に注意します。ユーザーも開発者には、動作や API の使用方法の変更が表示されます。 Windows 10 の作成者の更新プログラムで実行されているときに、新しい印刷スタックが既定で有効にします。 古い印刷スタックも引き続き古いバージョンの Windows で同じように動作します。|
|提案される解決策|古いスタックを Windows 10 の作成者の更新プログラムを使用する設定、<code>UseXpsOMPrinting</code>の REG_DWORD 値が、<code>HKEY_CURRENT_USER\Software\Microsoft\.NETFramework\Windows Presentation Foundation\Printing</code>レジストリ キーを<code>1</code>です。|
|スコープ|エッジ|
|Version|4.7|
|型|ランタイム|

