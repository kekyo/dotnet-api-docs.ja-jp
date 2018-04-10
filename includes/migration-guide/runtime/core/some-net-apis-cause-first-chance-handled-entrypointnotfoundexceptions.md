### <a name="some-net-apis-cause-first-chance-handled-entrypointnotfoundexceptions"></a>いくつか .NET Api 原因初回 (処理) EntryPointNotFoundExceptions

|   |   |
|---|---|
|説明|.NET Framework 4.5 で .NET メソッドの数が少ないが開始された最初の機会をスロー <xref:System.EntryPointNotFoundException?displayProperty=name>s。 これらの例外は .NET Framework 内で処理されますが、ファースト チャンス例外を予期していないテスト自動化を中断することがありました。 これらと同じ API は、HighVersionLie が有効なとき、一部の ApiVerifier シナリオを中断させます。|
|提案される解決策|このバグは、.NET Framework 4.5.1 にアップグレードすることによって回避できます。 テストの自動化を更新していない初回で中断する代わりに、 <xref:System.EntryPointNotFoundException?displayProperty=name>s。|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Diagnostics.Debug.Assert(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String,System.String)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String,System.String,System.Object[])?displayProperty=nameWithType></li><li><xref:System.Xml.Serialization.XmlSerializer.%23ctor(System.Type)?displayProperty=nameWithType></li></ul>|

