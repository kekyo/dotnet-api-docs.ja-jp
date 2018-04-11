### <a name="workflow-now-throws-original-exception-instead-of-nullreferenceexception-in-some-cases"></a>ワークフローは、場合によっては、NullReferenceException の代わりに元の例外ようになりましたがスローされます。

|   |   |
|---|---|
|説明|.NET Framework 4.6.2 ワークフロー アクティビティの Execute メソッドを使用して例外をスローした場合、以前のバージョンで、<code>null</code>値を<xref:System.Exception.Message>プロパティ、System.Activities ワークフロー ランタイムは、スロー、 <xref:System.NullReferenceException?displayProperty=name>、マスク、元の例外。 .NET Framework 4.7 以前マスクは、例外がスローされます。|
|提案される解決策|処理のコードが依存している場合、 <xref:System.NullReferenceException?displayProperty=name>、でした、カスタム アクティビティからスローされる例外をキャッチするように変更します。|
|スコープ|マイナー|
|Version|4.7|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Activities.CodeActivity.Execute(System.Activities.CodeActivityContext)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity%601.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.WorkflowInvoker.Invoke?displayProperty=nameWithType></li></ul>|

