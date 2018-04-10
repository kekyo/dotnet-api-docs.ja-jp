### <a name="appdomainsetupdynamicbase-is-no-longer-randomized-by-userandomizedstringhashalgorithm"></a>AppDomainSetup.DynamicBase が不要になった UseRandomizedStringHashAlgorithm でランダム化されました。

|   |   |
|---|---|
|説明|.NET Framework 4.6 の値の前に<xref:System.AppDomainSetup.DynamicBase>UseRandomizedStringHashAlgorithm アプリの構成ファイルに有効であった場合、アプリケーション ドメイン間またはプロセス間でランダム化はします。 以降、.NET Framework 4.6 で<xref:System.AppDomainSetup.DynamicBase>アプリの実行中の異なるインスタンス間で、別のアプリ ドメイン間に安定した結果が返されます。 別のアプリです。 この動的ベースが異なりますこの変更は、同じアプリの異なるインスタンスのランダムな名前付けの要素を削除するだけです。|
|提案される解決策|注意してくださいできる<code>UseRandomizedStringHashAlgorithm</code>は発生しません<xref:System.AppDomainSetup.DynamicBase>ランダム化されています。 ランダムなベースは、必要な場合は、この API を使用してではなく、アプリのコードで生成する必要があります。|
|スコープ|エッジ|
|Version|4.6|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.AppDomainSetup.DynamicBase?displayProperty=nameWithType></li></ul>|

