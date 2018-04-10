### <a name="enumerableemptylttresultgt-always-returns-cached-instance"></a>Enumerable.Empty&lt;TResult&gt;常にインスタンスのキャッシュを返します。

|   |   |
|---|---|
|説明|.NET 4.5 以降で<xref:System.Linq.Enumerable.Empty%60%601>常にキャッシュされた内部インスタンスを返します<xref:System.Collections.Generic.IEnumerable%601>です。以前は、<xref:System.Linq.Enumerable.Empty%60%601>空キャッシュ<xref:System.Collections.Generic.IEnumerable%601>API が呼び出された時点で、一部の条件をことを意味<xref:System.Linq.Enumerable.Empty%60%601>が呼び出された迅速にし、同時に、異なる型のインスタンスを別の呼び出しに対して返される可能性があります、API です。|
|提案される解決策|以前の動作は非確定的なため、コードがそれに依存している可能性は低いです。 ただし、ありそうにないことですが、空の列挙が比較され、ときには等しくないことが予期されている場合には、<xref:System.Linq.Enumerable.Empty%60%601> を使用する代わりに、明示的に空の配列を作成する (<code>new T[0]</code>) 必要があります。|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Linq.Enumerable.Empty%60%601?displayProperty=nameWithType></li></ul>|

