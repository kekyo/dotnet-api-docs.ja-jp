### <a name="rsacng-now-correctly-loads-rsa-keys-of-non-standard-key-size"></a>今すぐ RSACng 正しく、非標準のキー サイズの RSA キーを読み込みます

|   |   |
|---|---|
|説明|4.6.2 する前に .NET Framework のバージョンも RSA 証明書のキー サイズが非標準の顧客を使用してこれらのキーにアクセスできなければ、<xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=name>と<xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPrivateKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=name>拡張メソッド。  A<xref:System.Security.Cryptography.CryptographicException?displayProperty=name>メッセージ&quot;、要求されたキー サイズはサポートされていません&quot;がスローされます。 .NET Framework 4.6.2 でこの問題は修正されました。 同様に、<xref:System.Security.Cryptography.RSA.ImportParameters(System.Security.Cryptography.RSAParameters)>と<xref:System.Security.Cryptography.RSACng.ImportParameters(System.Security.Cryptography.RSAParameters)>スローされることがなくキーのサイズが標準で使用できるよう<xref:System.Security.Cryptography.CryptographicException?displayProperty=name>s。|
|提案される解決策|すべての例外処理、以前の動作に依存するロジックがある場合で、<xref:System.Security.Cryptography.CryptographicException?displayProperty=name>標準以外のキー サイズを使用している場合にスローされるロジックの削除を検討してください。|
|スコープ|エッジ|
|Version|4.6.2|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Security.Cryptography.RSA.ImportParameters(System.Security.Cryptography.RSAParameters)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.ImportParameters(System.Security.Cryptography.RSAParameters)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPrivateKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=nameWithType></li></ul>|

