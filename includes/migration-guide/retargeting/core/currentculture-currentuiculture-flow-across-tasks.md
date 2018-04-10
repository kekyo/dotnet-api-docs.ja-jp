### <a name="currentculture-and-currentuiculture-flow-across-tasks"></a>タスクにわたって CurrentCulture、CurrentUICulture のフロー

|   |   |
|---|---|
|説明|以降、.NET Framework 4.6 で<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>と<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>されます。 スレッドの<xref:System.Threading.ExecutionContext?displayProperty=name>、非同期操作の間でフローがします。変更することを意味<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>または<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>が非同期的に実行される後のタスクに反映されます。 これは、.NET Framework の以前のバージョンの動作と異なります (リセットするよう<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>と<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>すべての非同期タスクで)。|
|提案される解決策|この変更によって影響を受けるアプリは目的を明示的に設定してを回避する可能性があります<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>または<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>非同期タスクの最初の操作として。 または、以前の動作 (されていないの<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> / <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>) は次の互換性スイッチを設定して有効にする可能性があります。<pre><code class="language-C#">AppContext.SetSwitch(&quot;Switch.System.Globalization.NoAsyncCurrentCulture&quot;, true);&#13;&#10;</code></pre>この問題は、.NET Framework 4.6.2 での WPF によって修正されました。 .NET Frameworks 4.6、4.6.1 経由でも修正されました[KB 3139549](https://support.microsoft.com/kb/3139549)です。 .NET 4.6 以降を対象とするアプリケーションが、WPF アプリケーションで、右側の動作を自動的に表示します。 <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> / <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>) ディスパッチャー操作間で保持されます。|
|スコープ|マイナー|
|Version|4.6|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=nameWithType></li><li><xref:System.Threading.Thread.CurrentCulture?displayProperty=nameWithType></li><li><xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=nameWithType></li><li><xref:System.Threading.Thread.CurrentUICulture?displayProperty=nameWithType></li></ul>|

