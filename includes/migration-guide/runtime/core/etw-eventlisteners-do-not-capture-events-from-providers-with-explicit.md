### <a name="etw-eventlisteners-do-not-capture-events-from-providers-with-explicit-keywords-like-the-tpl-provider"></a>ETW EventListeners (TPL プロバイダー) のような明示的なキーワードと一緒に使用するプロバイダーからのイベントをキャプチャしません

|   |   |
|---|---|
|説明|空白のキーワード マスクを持つ ETW EventListeners は、明示的なキーワードを持つプロバイダーからのイベントを正しくキャプチャしません。 .NET Framework 4.5 では、TPL プロバイダーは、明示的なキーワードを提供するようになり、この問題が発生しました。 .NET Framework 4.6 では、EventListeners が更新され、この問題は修正されました。|
|提案される解決策|この問題を回避するへの呼び出しを置換<xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)>を明示的に指定するオーバー ロードを EnableEvents への呼び出しで、&quot;キーワード&quot;を使用するためのマスク:<code>EnableEvents(eventSource, level, unchecked((EventKeywords)0xFFFFffffFFFFffff))</code>です。代わりに、この問題は、.NET Framework 4.6 で修正されており、.NET Framework のバージョンにアップグレードすることで対処することがあります。|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)?displayProperty=nameWithType></li></ul>|

