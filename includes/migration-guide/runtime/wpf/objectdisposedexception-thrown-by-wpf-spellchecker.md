### <a name="objectdisposedexception-thrown-by-wpf-spellchecker"></a>ObjectDisposedException WPF スペリングによってスローされます。

|   |   |
|---|---|
|説明|場合によっては WPF アプリケーションがクラッシュするとアプリケーションのシャット ダウン中に、<xref:System.ObjectDisposedException?displayProperty=name>スペリングによってスローされます。 これは固定で .NET 4.7 WPF 例外を適切に処理し、アプリケーションが不要になった悪影響を受けることを確認します。 不定期の初回例外によってデバッガーの下で実行されているアプリケーションで発生するが続行されることに注意してください。|
|提案される解決策|.NET 4.7 へのアップグレード|
|スコープ|エッジ|
|Version|4.6.1|
|型|ランタイム|

