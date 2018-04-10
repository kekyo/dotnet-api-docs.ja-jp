### <a name="new-ambiguous-dispatcherinvoke-overloads-could-result-in-different-behavior"></a>(あいまい) に新しい Dispatcher.Invoke オーバー ロードは、異なる動作を可能性があります。

|   |   |
|---|---|
|説明|.NET Framework 4.5 を追加する新しいオーバー ロード<xref:System.Windows.Threading.Dispatcher.Invoke%2A?displayProperty=nameWithType>型のパラメーターを含む<xref:System.Action>です。 既存のコードを再コンパイルすると、コンパイラが Dispatcher.Invoke メソッドの呼び出しを解決することが、<xref:System.Delegate>パラメーターを持つ Dispatcher.Invoke メソッドへの呼び出しとして、<xref:System.Action>パラメーター。 持つ Dispatcher.Invoke オーバー ロードへの呼び出し、<xref:System.Delegate>パラメーターが持つ Dispatcher.Invoke オーバー ロードの呼び出しとして解決される、<xref:System.Action>動作に次の相違点が発生する、パラメーター。<ul><li>例外が発生した場合、<xref:System.Windows.Threading.Dispatcher.UnhandledExceptionFilter> イベントと <xref:System.Windows.Threading.Dispatcher.UnhandledException> イベントは発生しません。 代わりに、例外は <xref:System.Threading.Tasks.TaskScheduler.UnobservedTaskException?displayProperty=name> イベントによって処理されます。</li><li><xref:System.Windows.Threading.DispatcherOperation.Result> などの一部のメンバーの呼び出しは、操作が完了するまでブロックされます。</li></ul>|
|提案される解決策|あいまいさ (および例外処理またはブロック動作における考えられる相違点) を回避するために、呼び出し元の Dispatcher.Invoke は Invoke 呼び出しの 2 番目のパラメーターとして空の object[] を渡すことで、.NET 4.0 メソッドのオーバーロードに解決されるようにできます。|
|スコープ|マイナー|
|Version|4.5|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Windows.Threading.Dispatcher.Invoke(System.Delegate,System.Object[])?displayProperty=nameWithType></li><li><xref:System.Windows.Threading.Dispatcher.Invoke(System.Delegate,System.TimeSpan,System.Object[])?displayProperty=nameWithType></li><li><xref:System.Windows.Threading.Dispatcher.Invoke(System.Delegate,System.TimeSpan,System.Windows.Threading.DispatcherPriority,System.Object[])?displayProperty=nameWithType></li><li><xref:System.Windows.Threading.Dispatcher.Invoke(System.Delegate,System.Windows.Threading.DispatcherPriority,System.Object[])?displayProperty=nameWithType></li></ul>|

