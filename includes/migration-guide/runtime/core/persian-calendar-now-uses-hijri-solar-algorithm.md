### <a name="persian-calendar-now-uses-the-hijri-solar-algorithm"></a>ペルシャ暦はイスラム暦の太陽アルゴリズムを使用するようになりました

|   |   |
|---|---|
|説明|.NET Framework 4.6 以降で、<xref:System.Globalization.PersianCalendar?displayProperty=name>クラスはイスラム暦の太陽アルゴリズムを使用します。 までの日付に変換する、<xref:System.Globalization.PersianCalendar?displayProperty=name>他の予定表が 1800 より前または 2023 (グレゴリオ暦) より後の日付の .NET Framework 4.6 にわずかに異なる結果先頭になる可能性があります。また、<xref:System.Globalization.PersianCalendar.MinSupportedDateTime>現在<code>March 22, 0622 instead of March 21, 0622</code>です。|
|提案される解決策|.NET 4.6 で PersianCalendar を使用するときには、一部の早い日付または遅い日付に若干の差が生じる場合があることに注意してください。 また、異なるバージョンの .NET Framework で実行する可能性のあるプロセス間で日付をシリアル化するときには、PersianCalendar の日付文字列として格納しないでください (これらの値が異なる場合があるため)。|
|スコープ|マイナー|
|Version|4.6|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Globalization.PersianCalendar?displayProperty=nameWithType></li></ul>|

