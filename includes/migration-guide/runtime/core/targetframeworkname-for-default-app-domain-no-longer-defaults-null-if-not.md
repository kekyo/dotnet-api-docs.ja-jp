### <a name="targetframeworkname-for-default-app-domain-no-longer-defaults-to-null-if-not-set"></a>既定のアプリ ドメイン TargetFrameworkName 不要になったの既定値は設定しない場合は null

|   |   |
|---|---|
|説明|<xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name>が明示的に設定されている場合を除き、既定のアプリ ドメインで以前 null でした。 以降、4.6 では、<xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name>の既定のアプリ ドメインのプロパティは、TargetFrameworkAttribute から派生した (存在する) 場合、既定値になります。 既定以外のアプリ ドメインは継続的に継承、 <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> (これは、4.6 で null が既定で) 既定のアプリ ドメインから明示的にオーバーライドされた場合を除き、します。|
|提案される解決策|<xref:System.AppDomainSetup.TargetFrameworkName> が既定で null に設定されることに依然しないように、コードを更新する必要があります。 このプロパティが引き続き null として評価される必要がある場合、明示的にその値に設定できます。|
|スコープ|エッジ|
|Version|4.6|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=nameWithType></li></ul>|

