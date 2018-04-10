### <a name="wpf-datatemplate-elements-are-now-visible-to-uia"></a>WPF DataTemplate 要素が UIA に表示されます。

|   |   |
|---|---|
|説明|以前は、<xref:System.Windows.DataTemplate?displayProperty=name>要素の UI オートメーションを使用する表示ができませんでした。 4.5 から、UI オートメーションは、これらの要素を検出します。 多くの場合に便利ですが、含まれていないために UIA ツリーに依存しているテストが壊れる可能性がこの<xref:System.Windows.DataTemplate?displayProperty=name>要素。|
|提案される解決策|UI オートメーションのテストが必要になるこのアプリの更新のために UIA ツリー今すぐ以前非表示<xref:System.Windows.DataTemplate?displayProperty=name>要素。 たとえば、いくつかの要素が互いに隣り合っていることを予期しているテストでは、以前は非表示であった UIA 要素が間にあることを予期する必要があります。 または、UIA 要素の特定のカウントまたはインデックスに依存するテストは、新しい値で更新しなければならないことがあります。|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Windows.DataTemplate.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.DataTemplate.%23ctor(System.Object)?displayProperty=nameWithType></li></ul>|

