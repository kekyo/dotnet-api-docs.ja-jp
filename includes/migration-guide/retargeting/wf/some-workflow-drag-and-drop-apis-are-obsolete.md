### <a name="some-workflow-drag-and-drop-apis-are-obsolete"></a>一部のワークフローのドラッグ アンド ドロップ Api は廃止されました

|   |   |
|---|---|
|説明|このワークフロー ドラッグ アンド ドロップ API は今後使用しませんあり 4.5 に対して、アプリが再構築する場合はコンパイラの警告が発生します。|
|提案される解決策|新しい<xref:System.Activities.Presentation.DragDropHelper?displayProperty=name>複数のオブジェクトで操作をサポートする Api を代わりに使用する必要があります。 または、ビルド警告を抑制するか、古いコンパイラを使用して警告を回避できます。 API は、まだサポートされています。|
|スコープ|マイナー|
|Version|4.5|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Activities.Presentation.DragDropHelper.DoDragMove(System.Activities.Presentation.WorkflowViewElement,System.Windows.Point)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetCompositeView(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDraggedModelItem(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDroppedObject(System.Windows.DependencyObject,System.Windows.DragEventArgs,System.Activities.Presentation.EditingContext)?displayProperty=nameWithType></li></ul>|

