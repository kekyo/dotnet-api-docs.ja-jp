### <a name="profiling-aspnet-mvc4-apps-can-lead-to-fatal-execution-engine-error"></a>実行エンジンの致命的なエラーにつながる可能性が ASP.Net MVC4 のアプリのプロファイリング

|   |   |
|---|---|
|説明|NGEN/Profile アセンブリを使用してプロファイラー、' 致命的な実行エンジンが例外 ' の起動時にプロファイリング対象の ASP.NET MVC4 アプリケーションがクラッシュする可能性があります。|
|提案される解決策|.NET Framework 4.5.2 では、この問題が解決します。 また、プロファイラーを指定してこの問題を回避可能性があります<code>COR_PRF_DISABLE_ALL_NGEN_IMAGES</code>そのイベント マスクにします。|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|

