### <a name="htmltextwriter-does-not-render-br-element-correctly"></a>HtmlTextWriter はレンダリングされません`<br/>`要素正しく

|   |   |
|---|---|
|説明|.NET Framework 4.6 以降では、<xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)> と <xref:System.Web.UI.HtmlTextWriter.RenderEndTag> を <code>&lt;BR /&gt;</code> 要素を指定して呼び出すと、<code>&lt;BR /&gt;</code> を 1 つだけ (2 つではなく) 正しく挿入します。|
|提案される解決策|アプリが余分な <code>&lt;BR /&gt;</code> タグに依存している場合は、<xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)> をもう一度呼び出す必要があります。 この動作の変更が別のオプションは、従来の動作を取得するために、.NET Framework の以前のバージョンを対象とするために、.NET Framework 4.6 以降を対象とするアプリのみに影響する注意してください。|
|スコープ|エッジ|
|Version|4.6|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)?displayProperty=nameWithType></li><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.Web.UI.HtmlTextWriterTag)?displayProperty=nameWithType></li></ul>|

