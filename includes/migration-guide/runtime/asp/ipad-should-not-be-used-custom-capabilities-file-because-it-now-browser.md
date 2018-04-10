### <a name="ipad-should-not-be-used-in-custom-capabilities-file-because-it-is-now-a-browser-capability"></a>ブラウザーの機能であるためには IPad のカスタム機能ファイルで使用する必要がありますはありません。

|   |   |
|---|---|
|説明|.NET 4.5 以降で、iPad は既定 ASP.NET ブラウザーの機能ファイル内の識別子のため、カスタムの機能ファイルで使用されません必要があります。|
|提案される解決策|IPad の動作を変更するには、事前に定義されたゲートウェイ refID の機能を設定する必要は iPad 固有の機能が必要な場合は、 &quot;IPad&quot;の代わりに、新しいを生成して&quot;IPad&quot;ユーザー エージェントによって ID一致します。|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|

