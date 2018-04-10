### <a name="serialport-background-thread-exceptions"></a>SerialPort バック グラウンド スレッド例外

|   |   |
|---|---|
|説明|作成されたスレッドのバック グラウンド<xref:System.IO.Ports.SerialPort>ストリームが不要になった OS 例外がスローされたときに、プロセスが終了します。作成されたバック グラウンド スレッドで、オペレーティング システムの例外がスローされたときに、.NET Framework 4.7 と以前のバージョンを対象とするアプリケーションでプロセスが終了した、<xref:System.IO.Ports.SerialPort>ストリーム。アプリケーションで対象とする .NET Framework 4.7.1 またはそれ以降のバージョンでは、OS のイベントをバック グラウンド スレッドが待機はアクティブなシリアル ポートに関連して、シリアル ポートの急激な削除などのいくつかの場合、クラッシュすることがします。|
|提案される解決策|アプリについては、.NET Framework 4.7.1 を対象とする、選択を解除することが望ましくない場合に、次を追加することで、例外処理、<code>&lt;runtime&gt;</code>のセクションで、<code>app.config</code>ファイル。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>対象とするアプリの .NET Framework の以前のバージョンが、.NET Framework 4.7.1 または実行例外には、次を追加することで処理にオプトインした後で、<code>&lt;runtime&gt;</code>のセクションで、<code>app.config</code>ファイル。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|スコープ|マイナー|
|Version|4.7.1|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.IO.Ports.SerialPort?displayProperty=nameWithType></li></ul>|

