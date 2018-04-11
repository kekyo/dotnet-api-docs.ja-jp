### <a name="resizing-a-grid-can-hang"></a>ハングする可能性がグリッドのサイズを変更します。

|   |   |
|---|---|
|説明|無限ループがレイアウトの中に発生することができます、<code>T:System.Windows.Controls.Grid</code>次の状況で。<ul><li>行の定義には、2 つが含まれている *-行は、MinHeight と、MaxHeight 両方の宣言します。</li><li>コンテンツ、*、行が対応する MaxHeight を超えていません。</li><li>最初の MinHeight グリッドの使用可能な高さを超えた (およびその他の固定または行の自動)</li><li>アプリの対象 .Net 4.7、または 4.7 割り当てアルゴリズムに設定してオプトインを指定 <code>Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=false</code></li></ul>3 つ以上の行または列の場合は似ています、ループも発生します。 .Net 4.7.1 で問題が解決します。|
|提案される解決策|.Net 4.7.1 にアップグレードします。  また、4.7 割り当てアルゴリズムを必要としない場合は、次の構成設定を使用できます。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|スコープ|エッジ|
|Version|4.7|
|型|ランタイム|

