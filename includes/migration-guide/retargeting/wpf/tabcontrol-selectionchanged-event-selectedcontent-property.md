### <a name="tabcontrol-selectionchanged-event-and-selectedcontent-property"></a>TabControl SelectionChanged イベントおよび SelectedContent プロパティ

|   |   |
|---|---|
|説明|.NET Framework 4.7.1、以降の<xref:System.Windows.Controls.TabControl>の値を更新、<xref:System.Windows.Controls.TabControl.SelectedContent>を発生させる前に、プロパティ、<xref:System.Windows.Controls.Primitives.Selector.SelectionChanged>イベント、その選択が変更されたときにします。 .NET Framework 4.7 と以前のバージョンでは、イベント後に SelectedContent への更新が発生しました。|
|提案される解決策|.NET Framework 4.7.1 対象または後で選択を解除このアプリを変更し、次のように追加することで従来の動作を使用して、<code>&lt;runtime&gt;</code>アプリケーション構成ファイルのセクション。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>以前は、.NET Framework 4.7 を対象とするアプリ 4.7.1 .NET Framework で実行されているまたは後で有効にできます、新しい動作に次の行を追加することによって、<code>&lt;runtime&gt;</code>アプリケーション持つファイルのセクション。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|スコープ|マイナー|
|Version|4.7.1|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Windows.Controls.TabControl.SelectedContent?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.Selector.SelectionChanged?displayProperty=nameWithType></li></ul>|

