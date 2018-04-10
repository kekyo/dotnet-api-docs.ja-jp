### <a name="no-longer-able-to-set-enableviewstatemac-to-false"></a>No longer able to set EnableViewStateMac to false

|   |   |
|---|---|
|説明|ASP.NET では、開発者は <code>&lt;pages enableViewStateMac=&quot;false&quot;/&gt;</code> または <code>&lt;@Page EnableViewStateMac=&quot;false&quot; %&gt;</code> を指定できなくなりました。 ビュー ステートのメッセージ認証コード (MAC) は、ビュー ステートが埋め込まれたすべての要求に強制されています。 EnableViewStateMac プロパティを明示的に設定するアプリのみ<code>false</code>が影響を受けます。|
|提案される解決策|EnableViewStateMac を想定して true に設定する必要があり、結果として得られる MAC エラーを解決する必要があります (」の説明に従って[このガイダンス](https://support.microsoft.com/kb/2915218)、MAC エラーの原因の詳細に応じて複数の解像度が含まれています)。|
|スコープ|Major|
|Version|4.5.2|
|型|ランタイム|

