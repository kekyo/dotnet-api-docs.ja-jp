### <a name="cspparametersparentwindowhandle-now-expects-hwnd-value"></a>CspParameters.ParentWindowHandle は、HWND 値ようになりましたが必要です。

|   |   |
|---|---|
|説明|<xref:System.Security.Cryptography.CspParameters.ParentWindowHandle> 、.NET Framework 2.0 で導入された値により、UI キーにアクセスするために必要になるように、親ウィンドウのハンドル値を登録するアプリケーション (入力を求める、暗証番号 (pin) などもダイアログに同意するもの) に指定されたウィンドウのモーダルの子として表示されます。以降、.NET Framework 4.7 を対象とするアプリでは、Windows フォーム アプリケーションを設定できます、<xref:System.Security.Cryptography.CspParameters.ParentWindowHandle>次のようにコードを持つプロパティ。<pre><code class="language-C#">cspParameters.ParentWindowHandle = form.Handle;&#13;&#10;</code></pre>.NET Framework の以前のバージョンである値が必要、<xref:System.IntPtr?displayProperty=name>メモリ内の位置を表す場所、 [HWND](https://msdn.microsoft.com/library/windows/desktop/aa383751.aspx#HWND)存在していた値。 プロパティをフォームに設定します。Windows 7 で処理し、以前のバージョンで、影響がなかったが Windows 8 およびそれ以降のバージョンでは、その結果、 &quot; <xref:System.Security.Cryptography.CryptographicException?displayProperty=name>: パラメーターが正しくありません。&quot;|
|提案される解決策|.NET 4.7 を対象とする、または以降、親ウィンドウとの関係を登録したいアプリケーションを簡略化された形式を使用することをお勧めします。<pre><code class="language-C#">cspParameters.ParentWindowHandle = form.Handle;&#13;&#10;</code></pre>ユーザーに渡す正しい値が値を保持するメモリ位置のアドレスが確認できている<code>form.Handle</code>の選択を解除動作の変更、AppContext スイッチを設定して<code>Switch.System.Security.Cryptography.DoNotAddrOfCspParentWindowHandle</code>に<code>true</code>です。<ol><li>プログラムによって設定 compat スイッチによって、AppContext 説明に従って[ここ](http://blogs.msdn.com/b/dotnet/archive/2015/04/29/net-announcements-at-build-2015.aspx#dotnet46)</li><li>app.config ファイルの <code>&lt;runtime&gt;</code> セクションに以下の行を追加する:</li></ol><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.DoNotAddrOfCspParentWindowHandle=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>逆に、下にある古いバージョンの .NET Framework アプリケーションのロードは、AppContext を設定できる場合に、.NET Framework 4.7 ランタイムで新しい動作を選択したいユーザーが切り替える<code>false</code>です。|
|スコープ|マイナー|
|Version|4.7|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Security.Cryptography.CspParameters.ParentWindowHandle?displayProperty=nameWithType></li></ul>|

