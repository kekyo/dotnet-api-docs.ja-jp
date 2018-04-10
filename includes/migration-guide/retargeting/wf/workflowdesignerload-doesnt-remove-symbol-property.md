### <a name="workflowdesignerload-doesnt-remove-symbol-property"></a>WorkflowDesigner.Load はシンボル プロパティを削除しません。

|   |   |
|---|---|
|説明|ワークフロー デザイナーで再ホストされた 3.5 ワークフローの読み込みで .NET Framework 4.5 を対象とする場合、<xref:System.Activities.Presentation.WorkflowDesigner.Load>メソッド、<xref:System.Xaml.XamlDuplicateMemberException?displayProperty=name>がワークフローの保存中にスローされます。|
|提案される解決策|このバグは、中心を設定して動作できるように、ワークフロー デザイナーで、.NET Framework 4.5 を対象とする場合にのみマニフェスト、 <code>WorkflowDesigner.Context.Services.GetService&lt;DesignerConfigurationService&gt;().TargetFrameworkName</code> 4.0 の .NET Framework.Alternatively を使用して、問題を回避することがあります、<xref:System.Activities.Presentation.WorkflowDesigner.Load(System.String)>ワークフローを読み込むメソッド代わりに<xref:System.Activities.Presentation.WorkflowDesigner.Load>です。|
|スコープ|Major|
|バージョン|4.5|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Activities.Presentation.WorkflowDesigner.Load?displayProperty=nameWithType></li></ul>|

