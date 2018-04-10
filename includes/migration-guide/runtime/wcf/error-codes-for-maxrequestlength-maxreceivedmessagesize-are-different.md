### <a name="error-codes-for-maxrequestlength-or-maxreceivedmessagesize-are-different"></a>MaxRequestLength または maxReceivedMessageSize のエラー コードが異なる

|   |   |
|---|---|
|説明|WCF ではメッセージを web サービスのインターネット インフォメーション サービス (IIS) または ASP.NET 開発サーバーでホストされている (ASP.NET) の maxRequestLength を超えることも (WCF) の maxReceivedMessageSize 別のエラー コーディング HTTP ステータス コード 400 (Bad Request は変更) 413 (Request Entity Too Large)、および、maxRequestLength または maxReceivedMessageSize 設定のいずれかを超えるメッセージをスロー、<xref:System.ServiceModel.ProtocolException?displayProperty=name>例外。 これには、転送モードがストリーミングされるケースが含まれます。|
|提案される解決策|この変更は、メッセージの長さが ASP.NET または WCF で許可されている制限を超えた場合のデバッグを容易にします。HTTP 400 状態コードに基づいて処理を実行するすべてのコードを変更する必要があります。|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|

