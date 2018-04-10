### <a name="improved-accessibility-for-some-net-sdk-tools"></a>一部の .NET SDK ツールの強化されたユーザー補助機能

|   |   |
|---|---|
|説明|.NET Framework sdk 4.7.1 svcconfigedit.exe および svctraceviewer.exe ツールは、さまざまなアクセシビリティの問題を修正して改良しました。 これらのほとんど定義されていない名前や正しく実装されていない特定の UI オートメーション パターンのような小さな問題が発生しました。 多くのユーザーは、これらの正しくない値を認識はありませんが、スクリーン リーダーなどの支援技術を使用してユーザーがこれら SDK のツールの検索より使いやすくします。 確かに、これらの修正プログラムは、キーボード フォーカスの注文のようないくつか以前の動作を変更します。これらのツールで、ユーザー補助の修正のすべてを取得するためには、app.config ファイルに、次を実行できます。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|スコープ|エッジ|
|Version|4.7.1|
|型|再ターゲット中|

