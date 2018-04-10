### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>例外処理 ImageSourceConverter.ConvertFrom からコードに NullReferenceException

|   |   |
|---|---|
|説明|例外処理のコードでエラー<xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)>が正しくない原因となった<xref:System.NullReferenceException?displayProperty=name>が目的の例外の代わりにスローされます (例: <xref:System.IO.DirectoryNotFoundException?displayProperty=name>、 <xref:System.IO.FileNotFoundException?displayProperty=name>)、この変更は、メソッドは、今すぐ、正しい例外をスローするようにそのエラーを解決します。既定の .NET Framework 4.6.2 を対象とするすべてのアプリケーションおよび以下は引き続きスロー<xref:System.NullReferenceException?displayProperty=name>互換性のため、開発者にとっての .NET Framework 4.7 以降の必要がありますを参照してください右 exceptions.// 置換空間に 'x' の該当する場合|
|提案される解決策|取得する元に戻す開発者<xref:System.NullReferenceException?displayProperty=name>と .NET Framework 4.7 を対象とすることができますを追加/マージがアプリケーションの App.config ファイルに、次の。<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|スコープ|エッジ|
|Version|4.7|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

