### <a name="changes-in-path-normalization"></a>パスの正規化の変更

|   |   |
|---|---|
|説明|以降をターゲットとする .NET Framework 4.6.2 アプリでは、ランタイムがパスを正規化する方法が変更されました。パスを正規化するには、対象のオペレーティング システムで有効なパスに準拠するように、パスまたはファイルを識別する文字列を変更する必要があります。 通常、正規化では次のことを行います。<ul><li>コンポーネントとディレクトリの区切り記号を正規化する。</li><li>現在のディレクトリを相対パスに適用する。</li><li>相対ディレクトリ (.) または、パス内の親ディレクトリ (.) を評価しています。</li><li>指定した文字をトリミングする。</li></ul>以降をターゲットとする .NET Framework 4.6.2 アプリでは、パスの正規化で次の変更は既定で有効にします。<ul><li>ランタイムはオペレーティング システムの [GetFullPathName](https://msdn.microsoft.com/library/windows/desktop/aa364963(v=vs.85).aspx) 関数に従って、パスを正規化します。</li><li>正規化では、ディレクトリ セグメントの末尾 (ディレクトリ名の末尾のスペースなど) がトリミングされなくなりました。</li><li>完全な信頼でのデバイス パスの構文のサポートを含む <code>\\.\</code> and, for file I/O APIs in mscorlib.dll, '\?'.</li><li>The runtime does not validate device syntax paths.</li><li>The use of device syntax to access alternate data streams is supported.</li></ul>These changes improve performance while allowing methods to access previously inaccessible paths. Apps that target the .NET Framework 4.6.1 and earlier versions but are running under the .NET Framework 4.6.2 or later are unaffected by this change.|
|提案される解決策|.NET Framework 4.6.2 対象または後で選択を解除このアプリを変更し、レガシ正規化を使用して、次のように追加することで、<code>&lt;runtime&gt;</code>アプリケーション構成ファイルのセクション。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.UseLegacyPathHandling=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>以前は、.NET Framework 4.6.1 を対象とするアプリ、.NET Framework 4.6.2 で実行されているまたは後でできます有効にするパスの正規化への変更に次の行を追加することによって、<code>&lt;runtime&gt;</code>アプリケーション持つファイルのセクション。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.UseLegacyPathHandling=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|スコープ|マイナー|
|Version|4.6.2|
|型|再ターゲット中|

