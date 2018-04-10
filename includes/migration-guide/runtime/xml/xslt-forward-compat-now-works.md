### <a name="xslt-forward-compat-now-works"></a>XSLT 前方 compat ようになりました

|   |   |
|---|---|
|説明|.NET Framework 4 では、XSLT 1.0 の上位互換性には、次の問題が必要があります。<ul><li>バージョンが 2.0 に設定されているときに、パーサーが認識できない XSLT 1.0 コンストラクトに遭遇すると、スタイル シートの読み込みが失敗していました。</li><li>スタイル シートのバージョンが 1.1 に設定されている場合、<code>xsl:sort</code> コンストラクトでデータを並べ替えることができませんでした。</li></ul>.NET Framework 4.5 でこれらの問題を修正すると、および XSLT 1.0 の上位互換モードが適切に動作します。|
|提案される解決策|データの並べ替えが異なる場合によっては xsl:sort が守られているようになりましたが、ほとんどのアプリが影響を受ける、する必要があります。 場合<code>xsl:sort</code>は 1.1 のスタイル シートで使用されているアプリがデータの並べ替え順序に依存していないことを確認します。 アプリは、並べ替えの動作、4.0 に依存する場合は、削除<code>xsl:sort</code>スタイル シートからです。|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Xml.Xsl.XslCompiledTransform?displayProperty=nameWithType></li></ul>|

