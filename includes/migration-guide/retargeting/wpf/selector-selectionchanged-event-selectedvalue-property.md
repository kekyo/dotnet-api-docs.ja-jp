### <a name="selector-selectionchanged-event-and-selectedvalue-property"></a>セレクター SelectionChanged イベントおよび SelectedValue プロパティ

|   |   |
|---|---|
|説明|以降で、.Net Framework 4.7.1、<xref:System.Windows.Controls.Primitives.Selector>の値は常に更新その<xref:System.Windows.Controls.Primitives.Selector.SelectedValue%2A>発生させる前にプロパティ、<xref:System.Windows.Controls.Primitives.Selector.SelectionChanged>イベント、その選択が変更されたときにします。 これにより、SelectedValue プロパティは、その他の選択のプロパティと一致 (<xref:System.Windows.Controls.Primitives.Selector.SelectedItem%2A>と<xref:System.Windows.Controls.Primitives.Selector.SelectedIndex%2A>)、これがイベントを発生させる前に更新します。ほとんどの場合、イベントの前に、.NET Framework 4.7 と以前のバージョンで SelectedValue への更新が発生したが、それは起こったこと、イベント後に変更することで、選択の変更が発生した場合、<xref:System.Windows.Controls.Primitives.Selector.SelectedValue%2A>プロパティです。|
|提案される解決策|.NET Framework 4.7.1 対象または後で選択を解除このアプリを変更し、次のように追加することで従来の動作を使用して、<code>&lt;runtime&gt;</code>アプリケーション構成ファイルのセクション。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>以前は、.NET Framework 4.7 を対象とするアプリ 4.7.1 .NET Framework で実行されているまたは後で有効にできます、新しい動作に次の行を追加することによって、<code>&lt;runtime&gt;</code>アプリケーション持つファイルのセクション。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|スコープ|マイナー|
|Version|4.7.1|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Windows.Controls.TabControl.SelectedContent?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.Selector.SelectionChanged?displayProperty=nameWithType></li></ul>|

