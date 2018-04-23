### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>ImageSourceConverter.ConvertFrom からの例外処理コード内の NullReferenceException

|   |   |
|---|---|
|説明|<xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)> の例外処理コード内のエラーにより、目的の例外ではなく不適切な <xref:System.NullReferenceException?displayProperty=name> がスローされていました (たとえば、<xref:System.IO.DirectoryNotFoundException?displayProperty=name> や <xref:System.IO.FileNotFoundException?displayProperty=name> など)。今回の変更では、メソッドが正しい例外をスローするようにエラーが修正されました。既定では .NET Framework 4.6.2 以前を対象とするすべてのアプリケーションが互換性維持のために引き続き <xref:System.NullReferenceException?displayProperty=name> をスローします。.NET Framework 4.7 以降を対象とする開発者は適切な例外であるか確認する必要があります。// 該当する場合は、スペースを 'x' に置き換えます。|
|提案される解決策|NET Framework 4.7 を対象とする場合に <xref:System.NullReferenceException?displayProperty=name> を取得する構成に戻したい開発者は、アプリケーションの App.config ファイルに次のコードを追加/マージします。<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|スコープ|エッジ|
|Version|4.7|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

