### <a name="reflection-objects-can-no-longer-be-passed-from-managed-code-to-out-of-process-dcom-clients"></a>アウト プロセス DCOM クライアントにマネージ コードからリフレクション オブジェクトが渡さ不要になったことができます。

|   |   |
|---|---|
|説明|リフレクション オブジェクトはマネージ コードからアウト プロセス DCOM クライアントに渡されなくなりました。 影響を受ける型は次のとおりです。<ul><li><xref:System.Reflection.Assembly?displayProperty=name></li><li><xref:System.Reflection.MemberInfo?displayProperty=name> (とその派生型を含む<xref:System.Reflection.FieldInfo?displayProperty=name>、 <xref:System.Reflection.MethodInfo?displayProperty=name>、 <xref:System.Type?displayProperty=name>、および<xref:System.Reflection.TypeInfo?displayProperty=name>)</li><li><xref:System.Reflection.MethodBody?displayProperty=name></li><li><xref:System.Reflection.Module?displayProperty=name></li><li><xref:System.Reflection.ParameterInfo?displayProperty=name>。</li></ul>オブジェクトの <code>IMarshal</code> の呼び出しは <code>E_NOINTERFACE</code> を返します。|
|提案される解決策|非リフレクション オブジェクトで動作するように、マーシャリング コードを更新します。|
|スコープ|マイナー|
|Version|4.6|
|型|ランタイム|

