### <a name="missing-target-framework-moniker-results-in-40-behavior"></a>不足しているターゲット フレームワーク モニカーが 4.0 の動作になります

|   |   |
|---|---|
|説明|アプリケーションは、せず、<xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>アセンブリ レベルで自動的に実行、.NET Framework 4.0 のセマンティクス (quirks) を使用して適用します。 高品質を確実には、ことをお勧めするバイナリはすべて明示的に属性を使用する<xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>でビルドされた .NET Framework のバージョンを示すです。 プロジェクト ファイルで、ターゲット フレームワーク モニカーを使用しては MSBuild に自動的に適用すると、<xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>です。|
|提案される解決策|A<xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>のいずれかまたはでターゲット フレームワークを指定することによって、アセンブリに直接属性を追加することによって、指定する必要があります、[プロジェクト ファイルまたは Visual Studio によってプロジェクトのプロパティの GUI](http://blogs.msdn.com/b/visualstudio/archive/2010/05/19/visual-studio- managed-multi-targeting-part-1-concepts-target-framework-moniker-target-framework.aspx)です。|
|スコープ|Major|
|バージョン|4.5|
|型|ランタイム|

