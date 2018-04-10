### <a name="winrt-stream-adapters-no-long-call-flushasync-automatically-on-close"></a>WinRT ストリーム アダプター長い形式でを呼び出す FlushAsync 自動的に閉じる

|   |   |
|---|---|
|説明|Windows ストア アプリ、Windows ランタイム ストリーム アダプターは不要になった Dispose メソッドから FlushAsync メソッドを呼び出します。|
|提案される解決策|この変更は透過的である必要があります。 開発者は次のようなコードを記述して以前の動作を復元できます。<pre><code class="language-csharp">using (var stream = GetWindowsRuntimeStream() as Stream)&#13;&#10;{&#13;&#10;// do something&#13;&#10;await stream.FlushAsync();&#13;&#10;}&#13;&#10;</code></pre>|
|スコープ|透明|
|Version|4.5.1|
|型|ランタイム|

