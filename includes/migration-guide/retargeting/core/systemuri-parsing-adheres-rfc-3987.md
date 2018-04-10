### <a name="systemuri-parsing-adheres-to-rfc-3987"></a>RFC 3987 に準拠して System.Uri の解析

|   |   |
|---|---|
|説明|.NET 4.5 では、URI 解析がいくつかの点で変更されました。 ただし、これらの変更は .NET 4.5 を対象としたコードのみに影響することに注意してください。 バイナリが .NET 4.0 を対象としている場合、以前の動作が実行されます。 .NET 4.5 での URI 解析の変更は次のとおりです。<ul><li>URI の解析は、正規化および RFC 3987 で最新の IRI 規則に従ってチェック文字に実行されます。</li><li>Unicode 正規形 C は、URI のホスト部分でのみ実行されます。</li><li>無効な mailto: Uri は、例外が発生するようになりました。</li><li>パス セグメントの最後に末尾のドットは今すぐ保存されます。</li><li><code>file://</code> Uri がエスケープしない、<code>?</code>文字です。</li><li>Unicode 制御文字<code>U+0080</code>を通じて<code>U+009F</code>はサポートされていません。</li><li>コンマ文字<code>,</code>または<code>%2c</code>は自動的にエスケープ解除されません。</li></ul>|
|提案される解決策|古い .NET 4.0 URI 解析セマンティクスが必要な場合 (めったにありません)、.NET 4.0 を対象とすることによって使用できます。 これを使用して、<xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>アセンブリ、または 'プロジェクトのプロパティ ページで、Visual Studio のプロジェクト システム UI。|
|スコープ|Major|
|バージョン|4.5|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Uri.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Uri.%23ctor(System.String,System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Uri.%23ctor(System.String,System.UriKind)?displayProperty=nameWithType></li><li><xref:System.Uri.%23ctor(System.Uri,System.String)?displayProperty=nameWithType></li><li><xref:System.Uri.TryCreate(System.String,System.UriKind,System.Uri@)?displayProperty=nameWithType></li><li><xref:System.Uri.TryCreate(System.Uri,System.String,System.Uri@)?displayProperty=nameWithType></li><li><xref:System.Uri.TryCreate(System.Uri,System.Uri,System.Uri@)?displayProperty=nameWithType></li></ul>|

