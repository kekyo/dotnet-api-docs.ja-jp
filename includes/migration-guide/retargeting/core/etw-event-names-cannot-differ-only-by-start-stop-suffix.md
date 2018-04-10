### <a name="etw-event-names-cannot-differ-only-by-a-start-or-stop-suffix"></a>ETW イベントの名前が"Start"または「停止」サフィックスだけが異なることはできません。

|   |   |
|---|---|
|説明|.NET Framework 4.6 および 4.6.1 では、ランタイムによってスローされる、<xref:System.ArgumentException>と Event Tracing for Windows (ETW) イベントの 2 つの名前だけが異なる、&quot;開始&quot;または&quot;停止&quot;サフィックス (1 つのイベントがを名前付き場合として<code>LogUser</code>で別の名前が<code>LogUserStart</code>)。 この場合、ランタイムはイベント ソースを作成できないため、ログ記録は生成できません。|
|提案される解決策|例外を防ぐためには、2 つのイベント名が異なることなしでのみを確認してください、&quot;開始&quot;または&quot;停止&quot;サフィックス。この要件は、.NET Framework 4.6.2; 以降の削除します。ランタイムはだけが異なるイベント名を区別できます、&quot;開始&quot;と&quot;停止&quot;サフィックス。|
|スコープ|エッジ|
|Version|4.6|
|型|再ターゲット中|

