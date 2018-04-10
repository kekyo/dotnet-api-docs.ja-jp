### <a name="sharing-session-state-with-aspnet-stateserver-requires-all-servers-in-the-web-farm-to-use-the-same-net-framework-version"></a>Asp.Net StateServer でセッション状態を共有するには、同じ .NET Framework のバージョンを使用する web ファーム内のすべてのサーバーが必要です。

|   |   |
|---|---|
|説明|有効にする場合<xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=name>状態のために正しく共有を同じバージョンの .NET Framework を使用する必要がありますすべて指定された web ファーム内のサーバーのセッションの状態します。|
|提案される解決策|同時に状態を共有する web サーバーに .NET Framework のバージョンにアップグレードすることを確認します。|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=nameWithType></li></ul>|

