### <a name="ef-no-longer-throws-for-queryviews-with-specific-characteristics"></a>EF をスローしなくの queryview 以外の特定の特性を持つ

|   |   |
|---|---|
|説明|Entity Framework がスローされなく、 <xref:System.StackOverflowException?displayProperty=name> 0..1 を使用して QueryView に関係するクエリをアプリが実行時に例外がクエリの一部として関連エンティティを含めるしようとしています。 ナビゲーション プロパティ。 たとえばを呼び出して<code>.Include(e =&gt; e.RelatedNavProp)</code>です。|
|提案される解決策|この変更は 1 にある QueryViews を使用するコードのみに影響-0..1 関係を呼び出すクエリの実行時にします。含まれます。 これにより信頼性が向上し、ほとんどすべてのアプリに対して透過的になります。 ただし、予期しない動作が発生する場合、次のエントリをアプリの構成ファイルの <code>&lt;appSettings&gt;</code> セクションに追加することにより、この変更を無効にできます。<pre><code class="language-xml">&lt;add key=&quot;EntityFramework_SimplifyUserSpecifiedViews&quot; value=&quot;false&quot; /&gt;&#13;&#10;</code></pre>|
|スコープ|エッジ|
|Version|4.5.2|
|型|ランタイム|

