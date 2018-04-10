### <a name="applicationfiltermessage-no-longer-throws-for-re-entrant-implementations-of-imessagefilterprefiltermessage"></a>IMessageFilter.PreFilterMessage 実装の再入可能なため Application.FilterMessage が不要になったがスローされます。

|   |   |
|---|---|
|説明|.NET Framework 4.6.1 する前に、通話<xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)>で、<xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)>呼び出される<xref:System.Windows.Forms.Application.AddMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name>または<xref:System.Windows.Forms.Application.RemoveMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name>(もの呼び出し中に<xref:System.Windows.Forms.Application.DoEvents>) が発生する、<xref:System.IndexOutOfRangeException?displayProperty=name>です。以降、.NET Framework 4.6.1 を対象とするアプリケーションでは、この例外がスローされなく、および再入可能なフィルター前述のようを使用できます。|
|提案される解決策|注意してくださいを<xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)>、再入操作のスローが不要になった<xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)>上で説明した動作です。 これは、.NET Framework 4.6.1 の選択を解除、変更対象とする .NET Framework 4.6.1.Apps (または古いフレームワークを対象とする可能性がありますオプトイン アプリ) を対象とするアプリケーションを使用して、 [DontSupportReentrantFilterMessage](~/docs/framework/migration-guide/mitigation-custom-imessagefilter-prefiltermessage-implementations.md#mitigation)互換性スイッチ。|
|スコープ|エッジ|
|Version|4.6.1|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)?displayProperty=nameWithType></li></ul>|

