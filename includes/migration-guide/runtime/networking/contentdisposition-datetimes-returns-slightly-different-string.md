### <a name="contentdisposition-datetimes-returns-slightly-different-string"></a>します。 DateTimes が若干異なる文字列を返します

|   |   |
|---|---|
|説明|文字列の形式<xref:System.Net.Mime.ContentDisposition?displayProperty=name>が更新されました、4.6 では、常の時間部分を表すために、 <xref:System.DateTime?displayProperty=name> 2 桁の数字とします。 これは、[RFC822](http://www.ietf.org/rfc/rfc0822.txt) と [RFC2822](http://www.ietf.org/rfc/rfc2822.txt) に準拠しています。 これにより、4.6 では、配置の時間要素の 1 つが午前 10 時より前のシナリオでは、<xref:System.Net.Mime.ContentDisposition.ToString> は少し異なる文字列を返します。 ContentDispositions がを介してを文字列に変換、ため、場合によってシリアル化されることに注意してください<xref:System.Net.Mime.ContentDisposition.ToString>運用、シリアル化、または GetHashCode 呼び出しをレビューする必要があります。|
|提案される解決策|異なるバージョンの .NET Framework からの ContentDispotisions の文字列表現が互いに正しく対応することを期待しないでください。 可能な場合は、比較を行う前に、文字列を ContentDispositions に戻してください。|
|スコープ|マイナー|
|Version|4.6|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Net.Mime.ContentDisposition.ToString?displayProperty=nameWithType></li><li><xref:System.Net.Mime.ContentDisposition.GetHashCode?displayProperty=nameWithType></li></ul>|

