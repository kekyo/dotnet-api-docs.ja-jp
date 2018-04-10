### <a name="aspnet-accessibility-improvements-in-net-471"></a>.NET 4.7.1 で ASP.NET ユーザー補助機能強化

|   |   |
|---|---|
|説明|.NET Framework 4.7.1 から始めて、ASP.NET が向上しました ASP.NET お客様のサポートが向上する Visual Studio でのユーザー補助テクノロジを ASP.NET Web コントロールを操作する方法。  次の変更が含まれます。<ul><li>詳細ビュー ウィザードの フィールドの追加 ダイアログや ListView ウィザードの ListView の構成 ダイアログ ボックスなどの変更をコントロール内の不足している UI ユーザー補助のパターンを実装します。</li><li>ハイ コントラスト モードでは、データ ページャー フィールド エディターなどの表示を向上させるために変更します。</li><li>DataPager コントロール、ObjectContext の構成 ダイアログで、またはデータ ソース構成ウィザードの データの選択項目を構成 ダイアログ ボックスのページャー フィールドの編集ウィザードの フィールド ダイアログと同様に、コントロールのキーボード ナビゲーションを向上させるために変更が発生します。</li></ul>|
|提案される解決策|<strong>これらの変更を有効または無効方法</strong>.NET Framework 4.7.1 をこれらの変更を享受する Visual Studio デザイナーで、実行する必要がありますまたはそれ以降。 Web アプリケーションでは、次の方法のいずれかでこれらの変更を活用できます。<ul><li>Visual Studio 2017 15.3 をインストールするか、後で、既定では次の AppContext スイッチを使用して新しいユーザー補助機能をサポートします。</li><li>追加することで、従来のユーザー補助機能の動作を除外、 <code>Switch.UseLegacyAccessibilityFeatures</code> AppContext スイッチを<code>&lt;runtime&gt;</code>devenv.exe.config ファイルでセクションに設定して<code>false</code>次の例を示します。</li></ul><pre><code class="language-xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;&#13;&#10;&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;...&#13;&#10;&lt;!-- AppContextSwitchOverrides value attribute is in the form of &#39;key1=true/false;key2=true/false&#39;  --&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;...;Switch.UseLegacyAccessibilityFeatures=false&quot; /&gt;&#13;&#10;...&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>4.7.1 .NET Framework を対象とするアプリケーションまたはそれ以降、従来の保持してユーザー補助機能の動作を有効にできます従来のユーザー補助機能を使用この AppContext スイッチを明示的に設定して<code>true</code>です。|
|スコープ|マイナー|
|Version|4.7.1|
|型|再ターゲット中|

