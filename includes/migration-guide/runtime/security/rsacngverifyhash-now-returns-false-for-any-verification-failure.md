### <a name="rsacngverifyhash-now-returns-false-for-any-verification-failure"></a>RSACng.VerifyHash すべての検証のエラーに対して False を返します

|   |   |
|---|---|
|説明|.NET Framework 4.6.2 以降では、このメソッドが戻る<strong>False</strong>署名自体が正しくフォーマットされている場合。 今すぐ false を返しますの検証に失敗しました。 .NET Framework 4.6 および 4.6.1 では、メソッドによってスローされる、<xref:System.Security.Cryptography.CryptographicException?displayProperty=name>署名自体が正しくフォーマットされている場合。|
|提案される解決策|すべてのコードの実行は処理によって異なります、<xref:System.Security.Cryptography.CryptographicException?displayProperty=name>検証が失敗した場合は、代わりに実行する必要がありますが返されます<strong>False</strong>です。|
|スコープ|マイナー|
|Version|4.6.2|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Security.Cryptography.RSACng.VerifyHash(System.Byte[],System.Byte[],System.Security.Cryptography.HashAlgorithmName,System.Security.Cryptography.RSASignaturePadding)?displayProperty=nameWithType></li></ul>|

