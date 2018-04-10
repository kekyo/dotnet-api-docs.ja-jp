### <a name="wf-serializes-expressionsliterallttgt-datetimes-differently-now-breaks-custom-xaml-parsers"></a>WF Expressions.Literal をシリアル化&lt;T&gt; DateTimes が異なるようになりました (カスタム XAML パーサーを中断)

|   |   |
|---|---|
|説明|関連付けられた<xref:System.Windows.Markup.ValueSerializer>オブジェクトに変換されます、<xref:System.DateTime?displayProperty=name>または<xref:System.DateTimeOffset?displayProperty=name>オブジェクトの 2 つ目と<xref:System.DateTime.Millisecond?displayProperty=name>コンポーネントは、0 以外と (用、<xref:System.DateTime?displayProperty=name>値) が<xref:System.DateTime.Kind>プロパティがプロパティ要素に指定されていません。文字列ではなく構文があります。 この変更により、<xref:System.DateTime?displayProperty=name> 値と <xref:System.DateTimeOffset?displayProperty=name> 値を往復させることができるようになります。 入力 XAML が属性構文であると想定するカスタム XAML パーサーは正しく機能しません。|
|提案される解決策|この変更により、<xref:System.DateTime?displayProperty=name> 値と <xref:System.DateTimeOffset?displayProperty=name> 値を往復させることができるようになります。 入力 XAML が属性構文であると想定するカスタム XAML パーサーは正しく機能しません。|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|

