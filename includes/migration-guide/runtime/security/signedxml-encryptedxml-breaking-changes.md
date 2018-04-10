### <a name="signedxml-and-encryptedxml-breaking-changes"></a>SignedXml と EncryptedXml 重大な変更

|   |   |
|---|---|
|説明|.NET framework 4.6.2 でセキュリティ修正プログラムで<xref:System.Security.Cryptography.Xml.SignedXml?displayProperty=name>と<xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=name>を別の実行時動作に先行します。 たとえば、オブジェクトに適用された<ul><li>ドキュメントが同じ複数の要素を持つ場合<code>id</code>属性、署名対象にしてこれらの要素のいずれか、署名のルートとして、ドキュメントは現在無効と見なされます。</li><li>参照内で非正規 XPath 変換アルゴリズムを使用してドキュメントを無効と見なされるようになりました。</li><li>参照内で非正規の XSLT 変換アルゴリズムを使用して、ドキュメントはについて検討します。 が無効です。</li><li>すべてのプログラムを利用して外部のリソースがデタッチされた署名はそうことできません。</li></ul>|
|提案される解決策|開発者は、の使用状況を確認する<xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform>と<xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform>から派生した型にも、<xref:System.Security.Cryptography.Xml.Transform>ドキュメントの受信者が処理できないためです。|
|スコープ|マイナー|
|Version|4.6.2|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Security.Cryptography.Xml.Transform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXPathTransform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform?displayProperty=nameWithType></li></ul>|

