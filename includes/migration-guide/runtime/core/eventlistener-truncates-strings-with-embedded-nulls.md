### <a name="eventlistener-truncates-strings-with-embedded-nulls"></a>EventListener に埋め込み null 値を含む文字列を切り捨てます。

|   |   |
|---|---|
|説明|<xref:System.Diagnostics.Tracing.EventListener?displayProperty=name> は、埋め込まれた null のある文字列を切り捨てます。 null 文字は <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> クラスでサポートされません。 変更は、プロセスの <xref:System.Diagnostics.Tracing.EventListener?displayProperty=name> データを読み取るために <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> を使用し、区切り記号として null 文字を使用するアプリにのみ影響します。|
|提案される解決策|<xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> データを更新する、可能であれば、埋め込まれた null 文字を使用しないようにします。|
|スコープ|エッジ|
|Version|4.5.1|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Diagnostics.Tracing.EventListener.%23ctor?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel,System.Diagnostics.Tracing.EventKeywords)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel,System.Diagnostics.Tracing.EventKeywords,System.Collections.Generic.IDictionary{System.String,System.String})?displayProperty=nameWithType></li></ul>|

