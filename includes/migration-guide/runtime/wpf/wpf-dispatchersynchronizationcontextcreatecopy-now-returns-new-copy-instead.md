### <a name="wpf-dispatchersynchronizationcontextcreatecopy-now-returns-a-new-copy-instead-of-the-current-instance"></a>WPF DispatcherSynchronizationContext.CreateCopy が現在のインスタンスではなく、新しいコピーを返すようになりました

|   |   |
|---|---|
|説明|.NET Framework 4 で<xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy>パフォーマンスの最適化として、主に、現在のインスタンスへの参照が返されます。 .NET Framework 4.5 では、これが新しいインスタンスになり、参照が等しければ、実行中のスレッドが正しい同期コンテキストにあると結論付けることが初めて可能になりました。  これらの参照の id を確認するコードが影響を受ける、可能性はほとんどありませんが、変更されるため、コードを呼び出す<xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy>以降、.NET Framework 4.5 に移行の一環としてテストする必要があります。|
|提案される解決策|注意してくださいを<xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy>は返します新しい<xref:System.Threading.SynchronizationContext?displayProperty=name>オブジェクト。 以前は、このように生成された参照の等価性を使用するコードは、実際には、正しいコンテキストにあるかどうかを確認していませんでしたが、.NET 4.5 以降でのビルド時には確認を行います。  問題になる可能性は低いですが、影響を受けるコードのパスをよく調べて、何か問題が生じないかどうか確認する必要があります。|
|スコープ|マイナー|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy?displayProperty=nameWithType></li></ul>|

