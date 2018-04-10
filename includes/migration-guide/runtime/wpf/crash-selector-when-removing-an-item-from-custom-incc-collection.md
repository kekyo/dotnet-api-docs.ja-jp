### <a name="crash-in-selector-when-removing-an-item-from-a-custom-incc-collection"></a>カスタム INCC コレクションから項目を削除するときに、セレクターでクラッシュします。

|   |   |
|---|---|
|説明|<code>T:System.InvalidOperationException</code>次の状況で発生することができます。<ul><li>ItemsSource、 <code>T:System.Windows.Controls.Primitives.Selector</code> 、コレクションのカスタム実装には、<code>T:System.Collections.Specialized.INotifyCollectionChanged</code>です。</li><li>選択した項目がコレクションから削除されます。</li><li><code>T:System.Collections.Specialized.NotifyCollectionChangedEventArgs</code>が<code>P:System.Collections.Specialized.NotifyCollectionChangedEventArgs.OldStartingIndex</code>(不明な位置を示す)-1 を = です。</li></ul>例外のコール スタックが System.Windows.Threading.Dispatcher.VerifyAccess() System.Windows.Controls.Primitives.Selector.GetIsSelected (DependencyObject で System.Windows.DependencyObject.GetValue (DependencyProperty dp) で始まります要素) .Net 4.5 でこの例外が発生した場合は、アプリケーションがある 1 つ以上のディスパッチャー スレッドです。 .Net 4.7 例外が 1 つのディスパッチャー スレッドとアプリケーションでも発生することができます。 .Net 4.7.1 で問題が解決します。|
|提案される解決策|.Net 4.7.1 にアップグレードします。|
|スコープ|マイナー|
|Version|4.7|
|型|ランタイム|

