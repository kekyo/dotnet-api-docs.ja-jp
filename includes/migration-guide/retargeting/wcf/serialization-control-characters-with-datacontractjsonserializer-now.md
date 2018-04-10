### <a name="serialization-of-control-characters-with-datacontractjsonserializer-is-now-compatible-with-ecmascript-v6-and-v8"></a>DataContractJsonSerializer と制御文字のシリアル化は ECMAScript V6 と V8 と互換性のあるようになりました

|   |   |
|---|---|
|説明|.NET framework 4.6.2 と以前のバージョンで、 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=name> \b、\f、ECMAScript V6 および V8 の標準との互換性ができるように、\t などのいくつかの特別なコントロール文字をシリアル化できませんでした。 .NET Framework 4.7 以降では、これらの制御文字のシリアル化、およびと互換性 ECMAScript V6 V8 です。|
|提案される解決策|.NET Framework 4.7 を対象とするアプリの場合は、この機能は既定で有効にします。 この動作が望ましくない場合は、app.config または web.config ファイルの <code>&lt;runtime&gt;</code> セクションに次の行を追加して、この機能を無効にすることができます。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Runtime.Serialization.DoNotUseECMAScriptV6EscapeControlCharacter=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|スコープ|エッジ|
|Version|4.7|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlDictionaryWriter,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlWriter,System.Object)?displayProperty=nameWithType></li></ul>|

