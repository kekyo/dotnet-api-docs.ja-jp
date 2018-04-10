### <a name="aescryptoserviceprovider-decryptor-provides-a-reusable-transform"></a>AesCryptoServiceProvider 復号化、再利用可能な変換を提供します。

|   |   |
|---|---|
|説明|以降、.NET Framework 4.6.2 を対象とするアプリで、<xref:System.Security.Cryptography.AesCryptoServiceProvider>復号化が再利用可能な変換を提供します。 <xref:System.Security.Cryptography.CryptoAPITransform.TransformFinalBlock(System.Byte[],System.Int32,System.Int32)?displayProperty=name> の呼び出しの後、変換は初期化し直され、再利用することができます。 呼び出すことによって、復号化を再利用しようとしたアプリについては、.NET Framework の以前のバージョンを対象とする、<xref:System.Security.Cryptography.CryptoAPITransform.TransformBlock(System.Byte[],System.Int32,System.Int32,System.Byte[],System.Int32)?displayProperty=name>への呼び出し後<xref:System.Security.Cryptography.CryptoAPITransform.TransformFinalBlock(System.Byte[],System.Int32,System.Int32)?displayProperty=name>スロー、<xref:System.Security.Cryptography.CryptographicException>または破損したデータを生成します。|
|提案される解決策|これは想定される動作なので、この変更の影響が最小限に抑える必要があります。以前の動作に依存するアプリケーションの選択を解除する次の構成設定を追加することで使用して、<code>&lt;runtime&gt;</code>アプリケーションの構成ファイルのセクション。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.AesCryptoServiceProvider.DontCorrectlyResetDecryptor=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>さらに、.NET Framework の以前のバージョンをターゲットが .NET Framework 4.6.2 以降の .NET Framework のバージョンで実行されているアプリケーションを有効にできますが、次の構成設定を追加することで、<code>&lt;runtime&gt;</code>のセクションで、アプリケーションの構成ファイル:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.AesCryptoServiceProvider.DontCorrectlyResetDecryptor=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|スコープ|マイナー|
|Version|4.6.2|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Security.Cryptography.AesCryptoServiceProvider.CreateDecryptor?displayProperty=nameWithType></li></ul>|

