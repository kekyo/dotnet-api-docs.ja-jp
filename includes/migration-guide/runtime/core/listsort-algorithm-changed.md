### <a name="listsort-algorithm-changed"></a>List.Sort アルゴリズムの変更

|   |   |
|---|---|
|説明|.NET Framework 4.5 以降で<xref:System.Collections.Generic.List%601?displayProperty=name>の (クイック ソートの代わりに内省的での並べ替えに) 並べ替えアルゴリズムが変更されます。 <xref:System.Collections.Generic.List%601?displayProperty=name>並べ替えは、安定したなりましたが、この変更が不安定な方法で並べ替えるにはさまざまなシナリオが発生する可能性があります。 単に、同等の項目は、API の後続の呼び出しで異なる順序で並べ替えることができます。|
|提案される解決策|古いソート アルゴリズムがも安定して (が少し異なる方法)、コードと同等の項目が常に特定の順序で並べ替えが依存することはありません。 に応じてコードのインスタンスがあるし、以前の動作とラッキーされて、そのコードを更新するかが確定的に比較演算子を使用する場合は、目的の順序で並べ替えます。|
|スコープ|透明|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Collections.Generic.List%601.Sort?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Comparison{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Int32,System.Int32,System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li></ul>|

