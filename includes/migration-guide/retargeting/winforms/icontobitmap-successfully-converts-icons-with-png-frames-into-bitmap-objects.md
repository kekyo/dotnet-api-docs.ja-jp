### <a name="icontobitmap-successfully-converts-icons-with-png-frames-into-bitmap-objects"></a>Icon.ToBitmap がビットマップ オブジェクトに PNG フレームを含んだアイコンを正常に変換します。

|   |   |
|---|---|
|説明|以降、.NET Framework 4.6 を対象とするアプリで、<xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType>メソッドがビットマップ オブジェクトに PNG フレームを含んだアイコンを正常に変換します。 .NET Framework 4.5.2 および以前のバージョンを対象とするアプリで、<xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType>メソッドがスローされます、<xref:System.ArgumentOutOfRangeException>アイコン オブジェクトに PNG フレームがある場合は例外です。この変更はアプリを .NET Framework 4.6 を対象として再コンパイルして、特別な処理を実装している、<xref:System.ArgumentOutOfRangeException>アイコン オブジェクトに PNG フレームがある場合にスローされます。 .NET Framework 4.6 で実行している場合は、正常に変換が行われ、 <xref:System.ArgumentOutOfRangeException> がスローされることはないため、例外ハンドラーは呼び出されません。|
|提案される解決策|この動作が望ましくない場合は、次の要素を追加することによって、以前の動作を保持できます、 <code>&lt;runtime&gt;</code> app.config ファイルのセクション。<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true&quot; /&gt;&#13;&#10;</code></pre>App.config ファイルが既に含まれている場合、<code>AppContextSwitchOverrides</code>要素を新しい値は、次のように value 属性とマージする必要があります。<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true;&lt;previous key&gt;=&lt;previous value&gt;&quot; /&gt;&#13;&#10;</code></pre>|
|スコープ|マイナー|
|Version|4.6|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Drawing.Icon.ToBitmap?displayProperty=nameWithType></li></ul>|

