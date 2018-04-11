### <a name="horizontal-scrolling-and-virtualization"></a>水平方向にスクロールし、仮想化

|   |   |
|---|---|
|説明|この変更に適用されます、<xref:System.Windows.Controls.ItemsControl?displayProperty=name>直交するメインのスクロール方向の方向に独自の仮想化を行うこと (最高の例は<xref:System.Windows.Controls.DataGrid?displayProperty=name>EnableColumnVirtualization =&quot;True&quot;)。  より直感的な比較の垂直方向の操作の結果を結果を生成するために、特定の水平方向のスクロール操作の結果が変更されました。操作を含める&quot;スクロールは、ここ&quot;と&quot;右端&quot;、水平スクロール バーを右クリックして、メニューの名前を使用します。  これらの両方の計算、候補オフセットと呼び出し<xref:System.Windows.Controls.Primitives.IScrollInfo.SetHorizontalOffset(System.Double)>です。新しいオフセットの概念にスクロール後&quot;ここ&quot;または&quot;エッジを右&quot;の値を除外仮想化されたコンテンツが新しく変更されたために変更可能性がある<xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>です。 .Net 4.6.2 では、前に、スクロール操作だけを使用して候補のオフセットができない場合でも&quot;ここ&quot;または、&quot;エッジを右&quot;かを確認します。  これは、結果などの効果で&quot;バウンス&quot;スクロールのスクロール ボックス、最適な例をします。 <xref:System.Windows.Controls.DataGrid?displayProperty=name> ExtentWidth が = 1000 と幅 200 を = です。  スクロール&quot;右端&quot;1000 ~ 200 のオフセットは候補 800 を = です。  そのオフセットまでスクロールして、中に新しい列は de; は仮想化たとえばは非常に広いできるように、 <xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name> 2000年に変更します。  スクロールが HorizontalOffset で終わる = 800、およびつまみ&quot;bounces&quot;に中央のスクロール バーの正確に 800/2000 = 40%。変更では、新しい候補オフセットを再計算とこのような状況が発生すると、もう一度やり直してください。 (これは、どのように垂直方向のスクロール既に動作します)。変更には、エンド ユーザーより予測可能な直感的なエクスペリエンスが生成されますが、正確な値に依存するすべてのアプリにも影響でした<xref:System.Windows.Controls.Primitives.IScrollInfo.HorizontalOffset?displayProperty=name>を明示的に呼び出すまたはエンドユーザーで呼び出されたかどうか、水平方向にスクロール後<xref:System.Windows.Controls.Primitives.IScrollInfo.SetHorizontalOffset(System.Double)>です。|
|提案される解決策|予測値を使用するアプリ<xref:System.Windows.Controls.Primitives.IScrollInfo.HorizontalOffset?displayProperty=name>実際の値をフェッチに変更する必要があります (の値と<xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>) に影響する任意の水平スクロール後<xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>除外仮想化のためです。|
|スコープ|マイナー|
|Version|4.6.2|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Windows.Controls.Primitives.IScrollInfo?displayProperty=nameWithType></li></ul>|

