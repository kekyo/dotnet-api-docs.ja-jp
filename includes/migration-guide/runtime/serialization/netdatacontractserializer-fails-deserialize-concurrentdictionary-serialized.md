### <a name="netdatacontractserializer-fails-to-deserialize-a-concurrentdictionary-serialized-with-a-different-net-version"></a>NetDataContractSerializer が別の .NET バージョンでシリアル化された ConcurrentDictionary を逆シリアル化に失敗しました。

|   |   |
|---|---|
|説明|仕様では、<xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>両方、および逆シリアル化が終了は、同一の CLR 型を共有する場合にのみ使用できます。 そのため、これは保証されません、.NET Framework の 1 つのバージョンでシリアル化されたオブジェクトが、別のバージョンによって逆シリアル化することができます。<xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> .NET Framework 4.5 またはそれ以前をシリアル化し、.NET Framework 4.5.1 に逆シリアル化される場合、正しく逆シリアル化が正常にまたはそれ以降である型です。|
|提案される解決策|この問題の考えられる回避策の数があります。<ul><li>.NET Framework 4.5.1 にも使用するシリアル化するコンピューターをアップグレードします。</li><li>使用して<xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name>の代わりに<xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>正確な同一の CLR 型をシリアル化して終了を逆シリアル化の両方でこれが想定されていないようです。</li><li>使用して<xref:System.Collections.Generic.Dictionary%602?displayProperty=name>の代わりに<xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name>この特定 4.5 - 発生しないため&gt;4.5.1 を中断します。</li></ul>|
|スコープ|マイナー|
|Version|4.5.1|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Runtime.Serialization.NetDataContractSerializer.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li></ul>|

