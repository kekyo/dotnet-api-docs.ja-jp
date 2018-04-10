### <a name="deadlock-may-result-when-using-reentrant-services"></a>デッドロックが再入可能サービスの使用時になる可能性があります。

|   |   |
|---|---|
|説明|デッドロックは、再入可能サービスが含まれ、サービスのインスタンスを同時実行の 1 つのスレッドに制限があります。 この問題が発生しやすいサービスは、次の準備<xref:System.ServiceModel.ServiceBehaviorAttribute>がコード内。<pre><code class="language-csharp">[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Reentrant)]&#13;&#10;</code></pre>|
|提案される解決策|この問題に対処するには、次の操作を行うことができます。<ul><li>サービスの同時実行モードを設定<xref:System.ServiceModel.ConcurrencyMode.Single?displayProperty=nameWithType>または&lt;System.ServiceModel.ConcurrencyMode.Multiple?displayProperty=nameWithType&gt;です。 例:</li></ul><pre><code class="language-csharp">[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Single)]&#13;&#10;</code></pre><ul><li>.NET framework 4.6.2、最新の更新プログラムをインストールまたは .NET Framework の以降のバージョンにアップグレードします。 フローが無効になります、<xref:System.Threading.ExecutionContext>で<xref:System.ServiceModel.OperationContext.Current?displayProperty=nameWithType>です。 この動作は構成可能です。次のアプリケーション設定を構成ファイルに追加すると等価であります。</li></ul><pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&quot; value=&quot;true&quot; /&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;&#13;&#10;The value of &#39;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&#39; should never be set to &#39;false&#39; for Rentrant services.&#13;&#10;</code></pre>|
|スコープ|マイナー|
|Version|4.6.2|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.ServiceModel.ServiceBehaviorAttribute?displayProperty=nameWithType></li><li><xref:System.ServiceModel.ConcurrencyMode.Reentrant?displayProperty=nameWithType></li></ul>|

