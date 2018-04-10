### <a name="systemuriiswellformeduristring-method-returns-false-for-relative-uris-with-a-colon-char-in-first-segment"></a>最初のセグメントのコロン文字と相対 Uri System.Uri.IsWellFormedUriString メソッドが false を返します

|   |   |
|---|---|
|説明|.NET Framework 4.5 以降では<xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)>と相対 Uri を扱う、<code>:</code>形式が正しくないと、最初のセグメントにします。 これは変更されてから<xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name>RFC3986 に準拠するように行われた .NET Framework 4.0 で動作します。|
|提案される解決策|ようなその他の多くの変更の URI では) この変更は、.NET Framework 4.5 (またはそれ以降) を対象とするアプリケーションには影響のみ。 引き続き、以前の動作を使用して、.NET Framework 4.0 に対してアプリを対象します。 代わりに、URI の呼び出す前にスキャン<xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name>探して<code>:</code>可能性がありますを削除する検証のために、従来の動作が望ましい場合文字です。|
|スコープ|マイナー|
|Version|4.5|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=nameWithType></li></ul>|

