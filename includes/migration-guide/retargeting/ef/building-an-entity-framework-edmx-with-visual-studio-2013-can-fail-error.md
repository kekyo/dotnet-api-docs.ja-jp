### <a name="building-an-entity-framework-edmx-with-visual-studio-2013-can-fail-with-error-msb4062-if-using-the-entitydeploysplit-or-entityclean-tasks"></a>EntityDeploySplit または EntityClean タスクを使用した場合エラー msb 4062 で失敗することができます、Entity Framework edmx Visual Studio 2013 でのビルド

|   |   |
|---|---|
|説明|MSBuild 12.0 ツール (Visual Studio 2013 に含まれる) には、古い Entity Framework のターゲット ファイルが無効になる原因と、MSBuild のファイルの場所が変更されました。 その結果、<code>EntityDeploySplit</code> および <code>EntityClean</code> タスクは、<code>Microsoft.Data.Entity.Build.Tasks.dll</code> を見つけられないために失敗します。 この区切りツールセット (MSBuild/VS) が変更されたためされている .NET Framework の変更のために注意してください。 開発者ツールをアップグレードしたときにのみ発生し、.NET Framework をアップグレード下だけでは発生しません。|
|提案される解決策|Entity Framework のターゲット ファイルは、.NET Framework 4.6 で新しい MSBuild レイアウト先頭を操作に固定されます。 このバージョンの Framework にアップグレードすることで、この問題は修正されます。 または、[この](http://stackoverflow.com/a/24249247/131944) 回避策を使用して、ターゲット ファイルに直接パッチを当てることができます。|
|スコープ|Major|
|Version|4.5.1|
|型|再ターゲット中|

