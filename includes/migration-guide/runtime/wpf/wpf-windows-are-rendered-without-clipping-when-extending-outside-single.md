### <a name="wpf-windows-are-rendered-without-clipping-when-extending-outside-a-single-monitor"></a>1 つのモニターの外側を拡張するとき、クリッピングなし WPF ウィンドウが表示されます。

|   |   |
|---|---|
|説明|実行では、.NET Framework 4.6 以降の Windows 8 で、マルチ モニターのシナリオで 1 つのディスプレイの外部で拡張すると、クリッピングなしウィンドウ全体が表示されます。 これは、1 つのディスプレイの範囲を超えて拡張 WPF ウィンドウがクリップは、.NET Framework の以前のバージョンと異なります。|
|提案される解決策|(またはないをクリップするかどうか) この動作を明示的に設定するを使用して、<code>&lt;EnableMultiMonitorDisplayClipping&gt;</code>内の要素<code>&lt;appSettings&gt;</code>かを設定して、アプリケーションの構成ファイルで、<code>EnableMultiMonitorDisplayClipping</code>アプリの起動時にプロパティです。|
|スコープ|マイナー|
|Version|4.6|
|型|ランタイム|

