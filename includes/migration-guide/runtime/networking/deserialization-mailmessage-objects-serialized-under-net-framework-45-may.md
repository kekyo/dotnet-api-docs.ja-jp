### <a name="deserialization-of-mailmessage-objects-serialized-under-the-net-framework-45-may-fail"></a>.NET Framework 4.5 でシリアル化した MailMessage オブジェクトの逆シリアル化が失敗します。

|   |   |
|---|---|
|説明|.NET Framework 4.5 以降では<xref:System.Web.Mail.MailMessage>オブジェクトが非 ASCII 文字を含めることができます。 .NET Framework 4 では、ASCII 文字しかサポートされていません。 <xref:System.Web.Mail.MailMessage> .NET Framework 4 では、非 ASCII 文字が含まれていると、.NET Framework 4.5 またはそれ以降はシリアル化するオブジェクトを逆シリアル化ことはできません。|
|提案される解決策|逆シリアル化時に、コードが例外処理が提供することを確認、<xref:System.Web.Mail.MailMessage>オブジェクト。|
|スコープ|マイナー|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Web.Mail.MailMessage?displayProperty=nameWithType></li></ul>|

