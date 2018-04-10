### <a name="change-in-behavior-for-taskwaitall-methods-with-time-out-arguments"></a>タイムアウト引数を持つ Task.WaitAll メソッドの動作を変更します。

|   |   |
|---|---|
|説明|Task.WaitAll 動作が行われたより一貫性のある .NET 4.5.In で .NET Framework 4 で、これらのメソッドの動作が矛盾していました。 タイムアウトの期限が切れたときに、メソッドを呼び出す前に完了した、またはキャンセルされたタスクが 1 つ以上ある場合、メソッドでは <xref:System.AggregateException?displayProperty=name> 例外がスローされていました。 タイムアウトの期限が切れると、メソッド呼び出しの前に完了またはキャンセルされたタスクはなかったが、メソッド呼び出し後に 1 つ以上のタスクがこれらの状態になると、メソッドは false を返しました。<br/><br/>.NET Framework 4.5 でこれらのメソッド オーバー ロードを返します、タイムアウトの期限が切れたし、スローされるときに、すべてのタスクが実行中の場合は false、 <xref:System.AggregateException?displayProperty=name> (メソッドの前後であったかに関係なく、入力タスクが取り消された場合にのみ例外呼び出す) その他のタスクがまだ実行されていないとします。|
|提案される解決策|場合、<xref:System.AggregateException?displayProperty=name>コード IsCanceled プロパティ経由で同じ検出を行う必要があります代わりに呼び出される WaitAll 呼び出しの前にキャンセルされたタスクを検出するための手段としてキャッチされているされました (例: です。Any(t =&gt; t.IsCanceled)) ため、待機中のすべてのタスクがタイムアウトする前に完了した場合、.NET 4.6 はその場合にスローのみです。|
|スコープ|マイナー|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32,System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.TimeSpan)?displayProperty=nameWithType></li></ul>|

