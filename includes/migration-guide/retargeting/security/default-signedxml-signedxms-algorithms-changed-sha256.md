### <a name="default-signedxml-and-signedxms-algorithms-changed-to-sha256"></a>変更するには SHA256 既定 SignedXML および SignedXMS のアルゴリズム

|   |   |
|---|---|
|説明|.NET Framework 4.7 以前のバージョンで SignedXML と SignedCMS の既定値には SHA1 をいくつかの操作です。以降、.NET Framework 4.7.1 では、既定では、これらの操作には SHA256 が有効にします。 この変更は、SHA1 が不要になったと見なされるためセキュリティで保護された必要があります。|
|提案される解決策|SHA1 (安全でない) または SHA256 が既定で使用されるかどうかは、コントロールに新しいコンテキスト スイッチ値を 2 つがあります。<ul><li>Switch.System.Security.Cryptography.Xml.UseInsecureHashAlgorithms</li><li>Switch.System.Security.Cryptography.Pkcs.UseInsecureHashAlgorithms</li></ul>対象とする .NET Framework 4.7.1 と以降のバージョンでは、SHA256 の使用に適さない場合復元できる既定値は SHA1 を次の構成を追加することでアプリケーションに切り替え、[ランタイム](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)アプリケーションの構成のセクションファイル:<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.UseInsecureHashAlgorithms=true;Switch.System.Security.Cryptography.Pkcs.UseInsecureHashAlgorithms=true&quot; /&gt;&#13;&#10;</code></pre>次の構成スイッチを追加することによって、.NET Framework 4.7 と以前のバージョンを対象とするアプリケーションでこの変更を選択できます、[ランタイム](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)アプリ構成ファイルのセクション。<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.UseInsecureHashAlgorithms=false;Switch.System.Security.Cryptography.Pkcs.UseInsecureHashAlgorithms=false&quot; /&gt;&#13;&#10;</code></pre>|
|スコープ|マイナー|
|Version|4.7.1|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Security.Cryptography.Pkcs.CmsSigner?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.SignedXml?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.Reference?displayProperty=nameWithType></li></ul>|

