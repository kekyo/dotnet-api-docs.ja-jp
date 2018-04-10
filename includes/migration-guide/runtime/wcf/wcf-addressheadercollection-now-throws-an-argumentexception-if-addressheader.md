### <a name="wcf-addressheadercollection-now-throws-an-argumentexception-if-an-addressheader-element-is-null"></a>WCF AddressHeaderCollection は、ArgumentException を addressHeader 要素が null の場合にスローようになりました

|   |   |
|---|---|
|説明|.NET Framework 4.7.1、以降の<xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})>コンス トラクターをスロー、<xref:System.ArgumentException>場合は、要素の 1 つ<code>null</code>です。 .NET Framework 4.7 と以前のバージョンでは、例外はスローされません。|
|提案される解決策|発生した場合の .NET Framework 4.7.1 またはそれ以降のバージョンでこの変更との互換性の問題、することができますオプトアウトというに次の行を追加することによって、 <code>&lt;runtime&gt;</code> app.config ファイルのセクション。<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableAddressHeaderCollectionValidation=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|スコープ|マイナー|
|Version|4.7.1|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})?displayProperty=nameWithType></li></ul>|

