### <a name="workflow-checksums-changed-from-md5-to-sha1"></a>ワークフローのチェックサム MD5 から SHA1 に変更されました

|   |   |
|---|---|
|説明|Visual Studio でデバッグをサポートするには、は、ワークフロー ランタイムは、ハッシュ アルゴリズムを使用して、ワークフロー インスタンスのチェックサムを生成します。 .NET Framework 4.6.2 以前のバージョンで、ワークフロー チェックサム ハッシュと、FIPS 対応のシステム上の問題の原因となった MD5 アルゴリズムが使用されます。 .NET Framework 4.7 以降では、アルゴリズムは、SHA1 です。 コードには、計算されたチェックサムが永続化された場合、互換性がありますされません。|
|提案される解決策|コードは、チェックサム エラーのためのワークフロー インスタンスを読み込むことが場合、は、設定を試みてください。、<code>AppContext</code>切り替える&quot;Switch.System.Activities.UseMD5ForWFDebugger&quot; true に設定します。コードに示します。<pre><code class="language-csharp">System.AppContext.SetSwitch(&quot;Switch.System.Activities.UseMD5ForWFDebugger&quot;, true);&#13;&#10;</code></pre>または構成します。<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Activities.UseMD5ForWFDebugger=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|スコープ|マイナー|
|Version|4.7|
|型|再ターゲット中|

