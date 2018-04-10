### <a name="opt-in-break-to-revert-from-different-45-sql-generation-to-simpler-40-sql-generation"></a>オプトインの中断から 4.5 別の SQL 生成 4.0 の SQL の生成を簡単に戻すには

|   |   |
|---|---|
|説明|JOIN ステートメントを生成し、呼び出しを含むクエリ最初に、制限操作へ今 OrderBy の使用をより単純な SQL を生成します。 .NET Framework 4.5 にアップグレードするは、これらのクエリは、以前のバージョンよりも複雑な SQL を生成します。|
|提案される解決策|既定では、この機能は無効です。 Entity Framework では、パフォーマンスが低下する追加の JOIN ステートメントを生成する場合は、次のエントリを追加することでこの機能を有効にできます、<code>&lt;appSettings&gt;</code>アプリケーション構成 (app.config) ファイルのセクション。<pre><code class="language-xml">&lt;add key=&quot;EntityFramework_SimplifyLimitOperations&quot; value=&quot;true&quot; /&gt;&#13;&#10;</code></pre>|
|スコープ|透明|
|Version|4.5.2|
|型|ランタイム|

