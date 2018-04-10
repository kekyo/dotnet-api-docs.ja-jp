### <a name="calling-createdefaultauthorizationcontext-with-a-null-argument-has-changed"></a>Null の引数を持つ CreateDefaultAuthorizationContext を呼び出すことが変更されました

|   |   |
|---|---|
|説明|実装、<xref:System.IdentityModel.Policy.AuthorizationContext?displayProperty=name>への呼び出しによって返される、<xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=name>引数には null authorizationPolicies と .NET Framework 4.6 では、その実装が変更されました。|
|提案される解決策|まれに、カスタム認証を使用する WCF アプリの動作に違いが生じる可能性があります。 このような場合は、2 つの方法のいずれかで、以前の動作を復元できます。<ol><li>4.6 よりも前のバージョンの .NET Framework を対象とするようにアプリを再コンパイルする。 IIS でホストされるサービスを使用して、 &lt;httpRuntime targetFramework =&quot;x.x&quot;  / &gt;を .NET Framework の以前のバージョンを対象とする要素。</li><li>app.config ファイルの <code>&lt;appSettings&gt;</code> セクションに以下の行を追加します: <code>&lt;add key=&quot;appContext.SetSwitch:Switch.System.IdentityModel.EnableCachedEmptyDefaultAuthorizationContext&quot; value=&quot;true&quot; /&gt;</code></li></ol>|
|スコープ|マイナー|
|Version|4.6|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=nameWithType></li></ul>|

