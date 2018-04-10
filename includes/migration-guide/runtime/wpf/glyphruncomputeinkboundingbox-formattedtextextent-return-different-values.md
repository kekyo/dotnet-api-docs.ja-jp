### <a name="glyphruncomputeinkboundingbox-and-formattedtextextent-return-different-values-beginning-in-net-45"></a>GlyphRun.ComputeInkBoundingBox() と FormattedText.Extent .NET 4.5 以降で別の値を返す

|   |   |
|---|---|
|説明|機能強化が加えられた<xref:System.Windows.Media.GlyphRun.ComputeInkBoundingBox>と<xref:System.Windows.Media.FormattedText.Extent>.NET Framework 4.5 での問題に対処、ボックスが含まれている場合によっては、.NET Framework 4.0 でのグリフには小さすぎます。 この結果、.NET Framework 4.5 以降では、いくつかの境界ボックスが大きくなり、UI のレイアウトにわずかな違いが生じます。|
|提案される解決策|いくつかのグリフの境界ボックスのサイズが大きくなったことに注意してください。 このような変更は、通常、プレゼンテーションおよびヒット ボックス テストを向上させますが、以前の (.NET 4.5 より前の) 動作が望ましい場合は、次のエントリをアプリの構成ファイルに追加することによって実現できます。<pre><code class="language-xml">&lt;appsettings&gt;&#13;&#10;&lt;add key=&quot;IncludeAllInkInBoundingBox&quot; value=&quot;false&quot;&gt;&#13;&#10;&lt;/appsettings&gt;&#13;&#10;</code></pre>|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Windows.Media.GlyphRun.ComputeInkBoundingBox?displayProperty=nameWithType></li><li><xref:System.Windows.Media.FormattedText.Extent?displayProperty=nameWithType></li></ul>|

