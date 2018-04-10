### <a name="a-concurrentdictionary-serialized-in-net-45-with-netdatacontractserializer-cannot-be-deserialized-by-net-451-or-452"></a>NetDataContractSerializer で .NET 4.5 でシリアル化 ConcurrentDictionary は .NET 4.5.1 または 4.5.2 で逆シリアル化することはできません。

|   |   |
|---|---|
|説明|内部変更の種類ににより<xref:System.Collections.Concurrent.ConcurrentDictionary%602>.NET Framework 4.5 でシリアル化されるオブジェクトを使用して、 <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> .NET Framework 4.5.1 または .NET Framework 4.5.2.Note で逆シリアル化することはできません、他の方向 (内を移動.NET Framework でのシリアル化 4.5.x と .NET Framework 4.5 で逆シリアル化) は動作します。 同様に、すべて 4.x バージョン間のシリアル化は、.NET Framework 4.6.Serializing と連携し、.NET Framework の 1 つのバージョンで逆シリアル化が影響を受けません。|
|提案される解決策|シリアル化および逆シリアル化する必要がある場合、 <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> 、.NET Framework 4.5 と .NET Framework 4.5.1/4.5.2 間、代替のシリアライザーと同様に、<xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name>または<xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name>の代わりに、シリアライザーを使用する必要があります、<xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>です。代わりに、この問題が .NET Framework 4.6 でアドレス指定されるため、.NET Framework のバージョンにアップグレードすることで解決可能性があります。|
|スコープ|マイナー|
|Version|4.5.1|
|型|ランタイム|

