### <a name="incorrect-implementation-of-memberdescriptorequals"></a>MemberDescriptor.Equals の実装が正しくないです。

|   |   |
|---|---|
|説明|元の実装&quot;Equals&quot;メソッドが比較のオブジェクトからの 2 つの別の文字列プロパティを比較する: カテゴリ名を説明する文字列。 修正プログラムは、比較する&quot;カテゴリ&quot;する最初のオブジェクトの&quot;カテゴリ&quot;、2 つ目のおよび&quot;説明&quot;に&quot;説明&quot;です。 4.6.2 を対象とする場合に、新しい動作を除外する場合は true または false が framework バージョン 4.6.2 を下回る場合にこの修正プログラムを有効にするのには、MemberDescriptorEqualsReturnsFalseIfEquivalent 構成値を設定できます。|
|提案される解決策|MemberDescriptor.Equals も false を返すことで、アプリケーションが依存している場合は、記述子は、それと同等と 4.6.2 を対象としているバージョンの .NET Framework では、いくつかのオプションがあります。<ol><li>比較するコードの変更を加える&quot;カテゴリ&quot;と&quot;説明&quot;Equals メソッドを実行する手動で他のフィールドです。</li><li>App.config ファイルに次の値を追加することでこの変更から除外します。</li></ol><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>アプリケーションがターゲット 4.6.1 または下位のバージョンの .NET Framework があり、この変更を有効になっている場合、app.config ファイルに次の値を追加することで false には互換性スイッチを設定できます。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|スコープ|エッジ|
|Version|4.6.2|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.ComponentModel.MemberDescriptor.Equals(System.Object)?displayProperty=nameWithType></li></ul>|

