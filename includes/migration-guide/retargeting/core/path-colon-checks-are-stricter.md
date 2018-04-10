### <a name="path-colon-checks-are-stricter"></a>パスがコロン チェックがより厳密です

|   |   |
|---|---|
|説明|.NET framework 4.6.2 で以前にサポートされていないパス (の両方の長さと形式) をサポートする多数の変更が行われました。 正しいドライブ (コロン) の区切り記号の構文の確認が行われましたより正確許容されるが使用されているいくつかの選択パス Api でいくつかの URI パスをブロックすることの副作用が必要があります。|
|提案される解決策|影響を受ける Api への URI の引き渡しを場合は、最初に有効なパスである文字列を変更します。<ul><li>Url からスキームを手動で削除する (例: 削除<code>file://</code>Url から)</li><li>URI を渡す、<xref:System.Uri>クラスし、使用 <xref:System.Uri.LocalPath></li></ul>代わりに、選択を解除する、新しいパスの正規化を設定して、 <code>Switch.System.IO.UseLegacyPathHandling</code> AppContext スイッチを true にします。|
|スコープ|エッジ|
|Version|4.6.2|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.IO.Path.GetDirectoryName(System.String)?displayProperty=nameWithType></li><li><xref:System.IO.Path.GetPathRoot(System.String)?displayProperty=nameWithType></li></ul>|

