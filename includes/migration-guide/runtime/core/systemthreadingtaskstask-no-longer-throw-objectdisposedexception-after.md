### <a name="systemthreadingtaskstask-no-longer-throw-objectdisposedexception-after-object-is-disposed"></a>System.Threading.Tasks.Task は、オブジェクトが破棄された後に不要になった ObjectDisposedException をスローします。

|   |   |
|---|---|
|説明|除く<xref:System.Threading.Tasks.Task.System%23IAsyncResult%23AsyncWaitHandle>、<xref:System.Threading.Tasks.Task?displayProperty=name>メソッドをスローしなく、<xref:System.ObjectDisposedException?displayProperty=name>例外オブジェクトが破棄された後にします。この変更は、キャッシュされたタスクの使用をサポートします。 たとえば、メソッドで新しいタスクを割り当てる代わりに、既に完了した操作を表す、キャッシュされたタスクを返すことができます。 これは、タスクの任意のコンシューマーによって破棄されてしまうと、使用不可能になってしまう以前の .NET Framework のバージョンでは不可能でした。|
|提案される解決策|タスク メソッドをスローしない可能性がありますに注意してください<xref:System.ObjectDisposedException?displayProperty=name>場合、オブジェクトが破棄されるときにします。 タスクの状態を明示的にチェックを更新する必要がある場合は、アプリによってされたタスクが破棄されたことを確認するには、この例外を使用して<xref:System.Threading.Tasks.Task.Status>です。|
|スコープ|マイナー|
|Version|4.5|
|型|ランタイム|

