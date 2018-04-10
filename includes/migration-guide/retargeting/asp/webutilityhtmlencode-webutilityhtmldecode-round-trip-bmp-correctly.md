### <a name="webutilityhtmlencode-and-webutilityhtmldecode-round-trip-bmp-correctly"></a>WebUtility.HtmlEncode および WebUtility.HtmlDecode ラウンドト リップ BMP 正しく

|   |   |
|---|---|
|説明|.NET Framework 4.5、外側にある、基本的な (bmp: Multilingual Plane) のラウンドト リップ正しくに渡されるときに文字を対象とするアプリケーションの<xref:System.Net.WebUtility.HtmlDecode(System.String)>メソッドです。|
|提案される解決策|この変更が現在のアプリケーションには影響はありませんが、元の動作を復元するには設定する必要があります、<code>targetFramework</code>の属性、<code>&lt;httpRuntime&gt;</code>要素以外の文字列を&quot;4.5&quot;です。 また、.NET Framework の対象バージョンに関係なくこの動作を制御するために <code>unicodeEncodingConformance</code> 構成要素の <code>unicodeDecodingConformance</code> 属性と <code>&lt;webUtility&gt;</code> 属性を設定することもできます。|
|スコープ|エッジ|
|Version|4.5|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Net.WebUtility.HtmlEncode(System.String)?displayProperty=nameWithType></li><li><xref:System.Net.WebUtility.HtmlEncode(System.String,System.IO.TextWriter)?displayProperty=nameWithType></li></ul>|

