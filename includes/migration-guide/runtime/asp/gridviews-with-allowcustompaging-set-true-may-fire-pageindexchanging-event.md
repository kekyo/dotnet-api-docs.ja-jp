### <a name="gridviews-with-allowcustompaging-set-to-true-may-fire-the-pageindexchanging-event-when-leaving-the-final-page-of-the-view"></a>Gridview は true に設定するには、ビューの最後のページを終了するとき PageIndexChanging イベントを発生させる可能性があります。

|   |   |
|---|---|
|説明|.NET Framework 4.5 の不具合が原因で<xref:System.Web.UI.WebControls.GridView.PageIndexChanging?displayProperty=name>させる場合がありますいないを<xref:System.Web.UI.WebControls.GridView?displayProperty=name>が有効になっている s<xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=name>です。|
|提案される解決策|この問題は、.NET Framework 4.6 で修正されており、.NET Framework のバージョンにアップグレードすることで対処することがあります。 回避策としては、アプリがいずれかで、明示的な BindGrid を実行できる<code>Page_Load</code>これらの条件をヒットすると (、<xref:System.Web.UI.WebControls.GridView?displayProperty=name>は最後のページと最後に<xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name>とは異なる<xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name>)。 代わりに、そのシナリオが問題を再現していないように、アプリではなくカスタム ページング)、ページングを許可する変更できます。|
|スコープ|マイナー|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=nameWithType></li></ul>|

