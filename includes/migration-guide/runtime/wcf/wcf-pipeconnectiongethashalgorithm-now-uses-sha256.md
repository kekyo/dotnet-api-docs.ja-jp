### <a name="wcf-pipeconnectiongethashalgorithm-now-uses-sha256"></a>WCF PipeConnection.GetHashAlgorithm は SHA256 を使用するようになりました

|   |   |
|---|---|
|説明|以降、.NET Framework 4.7.1 では、Windows Communication Foundation は、名前付きパイプのランダムな名前を生成するのにには SHA256 ハッシュを使用します。 .NET Framework 4.7 と以前のバージョンでは、SHA1 ハッシュに使用します。|
|提案される解決策|.NET Framework 4.7.1 でこの変更に互換性の問題に実行するか、後ですることができますオプトアウトに次の行を追加することによって場合、 <code>&lt;runtime&gt;</code> app.config ファイルのセクション。<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InPipeConnectionGetHashAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|スコープ|マイナー|
|Version|4.7.1|
|型|ランタイム|

