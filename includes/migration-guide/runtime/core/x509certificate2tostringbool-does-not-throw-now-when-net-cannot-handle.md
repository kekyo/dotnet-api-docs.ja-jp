### <a name="x509certificate2tostringbool-does-not-throw-now-when-net-cannot-handle-the-certificate"></a>X509Certificate2.ToString(bool) では、.NET がときに、証明書に処理できないようになりましたはスローされません。

|   |   |
|---|---|
|説明|以前は、このメソッドはスロー <code>true</code> verbose パラメーターが渡されましたがあったと証明書をインストール、.NET Framework ではサポートされませんでした。 ここで、メソッドは成功し、証明書のアクセスの部分を省略する有効な文字列を返します。|
|提案される解決策|任意のコードによって<xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)>を API 以前をスローする場合に返される文字列が可能性があります (公開キー、秘密キーは、拡張機能など) の一部の証明書データを除外することを期待を更新する必要があります。|
|スコープ|エッジ|
|Version|4.6|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)?displayProperty=nameWithType></li></ul>|

