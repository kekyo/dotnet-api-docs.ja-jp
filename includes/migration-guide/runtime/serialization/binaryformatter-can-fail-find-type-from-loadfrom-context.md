### <a name="binaryformatter-can-fail-to-find-type-from-loadfrom-context"></a>LoadFrom コンテキストから型を検索する BinaryFormatter が失敗します。

|   |   |
|---|---|
|説明|.NET Framework 4.5、さまざまな時点で<xref:System.Xml.Serialization.XmlSerializer?displayProperty=name>を使用する場合、変更の逆シリアル化で不一致が発生する<xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name>LoadFrom コンテキストに読み込まれた型をシリアル化を解除します。 これらの変更は、新しい方法に起因<xref:System.Xml.Serialization.XmlSerializer?displayProperty=name>読み込むようになって、種類が異なる動作が発生時に、<xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name>後でその型に逆シリアル化しようとしています。 既定のシリアル化バインダー自動的に検索されません LoadFrom コンテキストが、状況によっては XmlSerializer の従来の動作に基づいていた可能性があります。 型が別のコンテキストで読み込まれたアセンブリから読み込まれるときに、変更のため、<xref:System.IO.FileNotFoundException?displayProperty=name>スローされる可能性があります。|
|提案される解決策|この例外が表示される場合、<code>Binder</code>のプロパティ、<xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name>を適切な型を検索するカスタム バインダーに設定することができます。<pre><code class="language-C#">var formatter = new BinaryFormatter { Binder = new TypeFinderBinder() }&#13;&#10;</code></pre>カスタム バインダーから:<pre><code class="language-C#">public class TypeFinderBinder : SerializationBinder&#13;&#10;{&#13;&#10;private static readonly string s_assemblyName = Assembly.GetExecutingAssembly().FullName;&#13;&#10;&#13;&#10;public override Type BindToType(string assemblyName, string typeName)&#13;&#10;{&#13;&#10;return Type.GetType(String.Format(CultureInfo.InvariantCulture, &quot;{0}, {1}&quot;, typeName, s_assemblyName));&#13;&#10;}&#13;&#10;}&#13;&#10;</code></pre>|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Deserialize(System.IO.Stream,System.Runtime.Remoting.Messaging.HeaderHandler)?displayProperty=nameWithType></li></ul>|

