### <a name="dataobjectgetdata-now-retrieves-data-as-utf-8"></a>DataObject.GetData は utf-8 としてデータを取得するようになりました

|   |   |
|---|---|
|説明|対象とする .NET Framework 4 または .NET Framework 4.5.1 またはそれ以前のバージョンで実行されるアプリの<code>DataObject.GetData</code>HTML 形式のデータを ASCII 文字列として取得します。 その結果、非 ASCII 文字 (ASCII コードが 0x7F よりも大きい文字) は、次の 2 つのランダムな文字で表されます。 .NET Framework 4.5 またはそれ以降と .NET Framework 4.5.2 で実行を対象とするアプリの<code>DataObject.GetData</code>0x7F よりも大きい文字を正しく表している utf-8 として HTML 形式のデータを取得します。|
|提案される解決策|HTML 形式の文字列を使用するエンコーディングの問題を回避する方法を実装したかどうか (たとえば、HTML 文字列を明示的にエンコードすることによって、クリップボードから渡すことによって取得に<xref:System.Text.UTF8Encoding.GetString(System.Byte[],System.Int32,System.Int32)?displayProperty=name>) バージョン 4 から 4.5 へアプリを再ターゲットしているとします。回避策を削除する必要があります。従来の動作は、何らかの理由により必要なアプリはその動作を実現する、.NET Framework 4.0 を対象することができます。|
|スコープ|エッジ|
|Version|4.5.2|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Windows.DataObject.GetData(System.String)?displayProperty=nameWithType></li><li><xref:System.Windows.DataObject.GetData(System.Type)?displayProperty=nameWithType></li><li><xref:System.Windows.DataObject.GetData(System.String,System.Boolean)?displayProperty=nameWithType></li></ul>|

