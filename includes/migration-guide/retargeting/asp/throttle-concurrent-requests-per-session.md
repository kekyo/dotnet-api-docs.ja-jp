### <a name="throttle-concurrent-requests-per-session"></a>セッションあたりの同時実行される要求のスロットル

|   |   |
|---|---|
|説明|.NET Framework 4.6.2 で前に、ASP.NET が同じセッション Id で要求を順番に実行および ASP.NET は常に既定では cookie を Sessionid を発行します。 ページ時間が長い応答、だけ f5 キーを押して、ブラウザーでサーバーのパフォーマンスを大幅に低下にされます。 この修正プログラムをキューに置かれた要求を追跡および指定された制限を超えると、要求を終了するカウンターが追加されました。 既定値は 50 です。 制限に達した場合、イベント ログ、および HTTP 500 応答を IIS ログに記録される可能性がありますに警告が記録されます。|
|提案される解決策|以前の動作を復元するには、次の設定を web.config ファイルに追加して、新しい動作を無効にできます。<pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;aspnet:RequestQueueLimitPerSession&quot; value=&quot;2147483647&quot;/&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;</code></pre>|
|スコープ|エッジ|
|Version|4.7|
|型|再ターゲット中|

