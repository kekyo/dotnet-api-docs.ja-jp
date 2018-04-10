### <a name="soapformatter-cannot-deserialize-hashtable-and-similar-ordered-collection-objects"></a>ハッシュ テーブルの逆シリアル化できません SoapFormatter およびのような順序付けコレクション オブジェクト

|   |   |
|---|---|
|説明|<xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name>オブジェクトが 1 つの .NET Framework のバージョンをシリアル化するという保証は異なるバージョンで正常に逆シリアル化しません。 コレクションを具体的には、いくつか順序付け (と同様に<xref:System.Collections.Hashtable?displayProperty=name>) 4.0 と 4.5 間のメンバーを追加など、.NET 4.5 でシリアル化された場合に、次のこれらの型のオブジェクトが .NET 4.0 で逆シリアル化できません。 シリアル化データのシリアル化と逆シリアル化の両方が同じバージョンの .NET Framework で行われた場合、問題は発生しないことに注意してください。|
|提案される解決策|<xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> シリアル化する必要がありますとの差し替え<xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name>シリアル化または<xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>.NET Framework の変更に対応できます。|
|スコープ|マイナー|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object,System.Runtime.Remoting.Messaging.Header[])?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream,System.Runtime.Remoting.Messaging.HeaderHandler)?displayProperty=nameWithType></li></ul>|

