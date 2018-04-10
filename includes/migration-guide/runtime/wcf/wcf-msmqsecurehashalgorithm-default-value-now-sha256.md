### <a name="wcf-msmqsecurehashalgorithm-default-value-is-now-sha256"></a>WCF MsmqSecureHashAlgorithm 既定値は SHA256

|   |   |
|---|---|
|説明|.NET Framework 4.7.1 から始めて、署名アルゴリズムは、WCF で Msmq メッセージの既定のメッセージは、SHA256 です。 .NET Framework 4.7 以前のバージョンで、既定のメッセージの署名アルゴリズムは SHA1 です。|
|提案される解決策|.NET Framework 4.7.1 でこの変更と互換性の問題に実行するか、後ですることができますオプトアウト変更には、次の行を追加することによって場合、 <code>&lt;runtime&gt;</code>app.config ファイルのセクション。<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InMsmqEncryptionAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|スコープ|マイナー|
|Version|4.7.1|
|型|ランタイム|

