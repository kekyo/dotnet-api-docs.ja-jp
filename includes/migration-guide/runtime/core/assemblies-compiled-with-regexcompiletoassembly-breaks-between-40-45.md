### <a name="assemblies-compiled-with-regexcompiletoassembly-breaks-between-40-and-45"></a>4.0 および 4.5 Regex.CompileToAssembly の区切り記号でコンパイルされたアセンブリ

|   |   |
|---|---|
|説明|コンパイルされる正規表現のアセンブリが .NET Framework 4.5 は .NET Framework 4 を対象に組み込まれている場合は、例外をスロー システム上で .NET Framework 4 アセンブリをインストールするには、正規表現のいずれかを使用しようとしています。|
|提案される解決策|この問題を回避するには、次のいずれかの方法を実行します。<ul><li>.NET Framework 4 の正規表現を含むアセンブリをビルドします。</li><li>解釈される正規表現を使用します。</li></ul>|
|スコープ|マイナー|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName)?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[])?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[],System.String)?displayProperty=nameWithType></li></ul>|

