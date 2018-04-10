### <a name="servicebase-doesnt-propagate-onstart-exceptions"></a>ServiceBase は、OnStart 例外を反映しません。

|   |   |
|---|---|
|説明|.NET Framework 4.7 以前のバージョンで、サービスの開始時にスローされる例外は反映されませんの呼び出し元に<xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType>です。以降、.NET Framework 4.7.1 を対象とするアプリケーションでは、ランタイムでに例外を反映<xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType>の起動に失敗するサービスです。|
|提案される解決策|サービスの開始時に、例外がある場合、その例外は反映されます。 サービスが開始に失敗した場合の診断に役立つこの必要があります。この動作が望ましくない場合は、選択を解除するが、次を追加することによって<AppContextSwitchOverrides>要素を<runtime>アプリケーション構成ファイルのセクション。<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=true&quot; /&gt;&#13;&#10;</code></pre>アプリケーションが 4.7.1 より前のバージョンを対象に、この動作する場合は、次のコードを追加<AppContextSwitchOverrides>要素を<runtime>アプリケーション構成ファイルのセクション。<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=false&quot; /&gt;&#13;&#10;</code></pre>|
|スコープ|マイナー|
|Version|4.7.1|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase)?displayProperty=nameWithType></li><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase[])?displayProperty=nameWithType></li></ul>|

