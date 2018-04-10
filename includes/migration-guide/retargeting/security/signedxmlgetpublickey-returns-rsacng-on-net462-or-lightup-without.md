### <a name="signedxmlgetpublickey-returns-rsacng-on-net462-or-lightup-without-retargeting-change"></a>SignedXml.GetPublicKey によって net462 (またはライトアップ) に再ターゲットの変更なし RSACng が返されます。

|   |   |
|---|---|
|説明|以降、.NET Framework 4.6.2、によって返されるオブジェクトの具体的な型で、<xref:System.Security.Cryptography.Xml.SignedXml.GetPublicKey%2A?displayProperty=nameWithType>メソッド (へことがなく変更特性) CryptoServiceProvider 実装から Cng 実装します。 これを使用してから、実装が変更されたため<code>certificate.PublicKey.Key</code>、内部使用に<code>certificate.GetAnyPublicKey</code>に転送する<xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey%2A?displayProperty=nameWithType>です。|
|提案される解決策|以降、.NET Framework 4.7.1 で実行されているアプリでは、既定では、.NET Framework 4.6.1 で使用される CryptoServiceProvider 実装を使用することができますし、次の構成を追加することによって、以前のバージョンに切り替えると、[ランタイム](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)アプリ構成ファイルのセクション。<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.SignedXmlUseLegacyCertificatePrivateKey=true&quot; /&gt;&#13;&#10;</code></pre>|
|スコープ|エッジ|
|Version|4.6.2|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Security.Cryptography.Xml.SignedXml.CheckSignatureReturningKey(System.Security.Cryptography.AsymmetricAlgorithm@)?displayProperty=nameWithType></li></ul>|

