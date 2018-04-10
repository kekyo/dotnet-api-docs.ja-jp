### <a name="the-default-hash-algorithm-for-wpf-packagedigitalsignaturemanager-is-now-sha256"></a>WPF PackageDigitalSignatureManager の既定のハッシュ アルゴリズムが SHA256 をします。

|   |   |
|---|---|
|説明|<code>System.IO.Packaging.PackageDigitalSignatureManager</code> WPF パッケージに関連してデジタル署名の機能を提供します。  .NET Framework 4.7 と以前のバージョンでは、既定のアルゴリズムで (<xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType>) には SHA1 がパッケージのパーツの署名に使用します。  SHA256 を最近使用したセキュリティ上の問題により SHA1 をこの既定値が変更された .NET Framework 4.7.1 以降します。  この変更は、すべてパッケージの署名、XPS ドキュメントを含むに影響します。|
|提案される解決策|下 4.7.1 の .NET framework のバージョンを対象とするときにこの変更を利用する開発者または .NET 4.7.1 または大きい値が対象とするときに以前の機能を必要とする開発者は、次の AppContext フラグを適切に設定します。  SHA1、値は true になります既定のアルゴリズムとして使用されている。false の結果には SHA256 になります。<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.UseSha1AsDefaultHashAlgorithmForDigitalSignatures=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|スコープ|エッジ|
|Version|4.7.1|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType></li></ul>|

