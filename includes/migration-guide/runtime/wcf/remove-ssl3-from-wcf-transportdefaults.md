### <a name="remove-ssl3-from-the-wcf-transportdefaults"></a>WCF TransportDefaults から Ssl3 を削除します。

|   |   |
|---|---|
|説明|トランスポート セキュリティで NetTcp を使用し、証明書の資格情報の種類を使用する場合、SSL 3 プロトコルは、安全な接続のネゴシエーションに使用される既定のプロトコルではなくなりました。 ほとんどの場合ことはありません既存のアプリに影響を与える NetTcp の TLS 1.0 がプロトコルの一覧に含まれて常にいるとします。 既存のすべてのクライアントは TLS 1.0 以降を使用して接続をネゴシエートできるようになりました。|
|提案される解決策|Ssl3 が必要な場合は、次の構成メカニズムのいずれかを使用して、Ssl3 をネゴシエートされたプロトコルの一覧に追加します。<ul><li><xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement.SslProtocols></li><li><xref:System.ServiceModel.TcpTransportSecurity.SslProtocols></li><li>[<](~/docs/framework/configure-apps/file-schema/wcf/transport-of-nettcpbinding.md)</li><li>[&lt;sslStreamSecurity&gt; section of &lt;customBinding&gt;]~/docs/framework/configure-apps/file-schema/wcf/sslstreamsecurity.md)</li></ul>|
|スコープ|エッジ|
|Version|4.6.2|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement.SslProtocols?displayProperty=nameWithType></li><li><xref:System.ServiceModel.TcpTransportSecurity.SslProtocols?displayProperty=nameWithType></li></ul>|

