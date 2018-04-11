### <a name="long-path-support"></a>長いパスのサポート

|   |   |
|---|---|
|説明|以降とするアプリをターゲットとする .NET Framework 4.6.2、長いパス (最大 32 K の文字) がサポートされている、および 260 文字 (または<code>MAX_PATH</code>) パスの長さの制限がなくなりました。 .NET Framework 4.6.2 を対象として再コンパイルされたアプリの場合は、コードをスローした以前のパス、 <xref:System.IO.PathTooLongException?displayProperty=name> 260 文字をスローがパスを超えたため、<xref:System.IO.PathTooLongException?displayProperty=name>次の条件下でのみ。<ul><li>パスの長さがより大きい<xref:System.Int16.MaxValue>(32,767) 文字です。</li><li>オペレーティング システムが <code>COR_E_PATHTOOLONG</code> またはそれと同等のものを返す。</li></ul>.NET Framework 4.6.1 と以前のバージョンを対象とするアプリの場合、ランタイムが自動的をスロー、<xref:System.IO.PathTooLongException?displayProperty=name>されるたびに、パスが 260 文字を超えています。|
|提案される解決策|.NET Framework 4.6.2 を対象とするアプリの場合は、選択を解除する長いパス サポートこれが望ましくない場合に、次を追加することによって、<code>&lt;runtime&gt;</code>のセクションで、<code>app.config</code>ファイル。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.BlockLongPaths=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>対象とするアプリ用 .NET Framework 4.6.2 では、.NET Framework の以前のバージョンを実行または後を選択できます長いパスをサポートするには、次を追加することによって、<code>&lt;runtime&gt;</code>のセクションで、<code>app.config</code>ファイル。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.BlockLongPaths=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|スコープ|マイナー|
|Version|4.6.2|
|型|再ターゲット中|

