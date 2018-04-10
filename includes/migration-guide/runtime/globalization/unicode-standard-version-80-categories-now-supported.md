### <a name="unicode-standard-version-80-categories-now-supported"></a>Unicode 標準バージョン 8.0 カテゴリのようになりました

|   |   |
|---|---|
|説明|.NET framework 4.6.2、フレームワーク内の Unicode データはアップグレードされて Unicode 標準 version 6.3 から version 8.0 に。  .NET Framework 4.6.2 で Unicode 文字カテゴリを要求すると、いくつかの結果が以前のバージョンの .NET Framework での結果一致しません。  これは、影響チェロキー音節と新しい末尾 Lue 母音記号とトーン マークほとんどの場合に変更します。|
|提案される解決策|コードを確認し、ハード コーディングされた Unicode 文字カテゴリに依存するロジックの削除/変更するとします。|
|スコープ|マイナー|
|Version|4.6.2|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Char.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.String,System.Int32)?displayProperty=nameWithType></li></ul>|

