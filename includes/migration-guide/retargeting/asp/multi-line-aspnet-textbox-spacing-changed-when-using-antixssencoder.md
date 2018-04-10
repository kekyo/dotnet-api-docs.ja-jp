### <a name="multi-line-aspnet-textbox-spacing-changed-when-using-antixssencoder"></a>複数行テキスト ボックスの ASP.Net 間隔 AntiXSSEncoder を使用する場合の変更

|   |   |
|---|---|
|説明|.NET Framework 4.0 では、<xref:System.Web.Security.AntiXss.AntiXssEncoder?displayProperty=name> を使用する場合、ポストバックの複数行テキスト ボックスの行間に余分な行が挿入されました。 .NET Framework 4.5 では、これらの余分な改行は含まれませんが、web アプリが .NET 4.5 を対象としている場合に限ります。|
|提案される解決策|4.0 の Web アプリの対象を .NET 4.5 に変更すると、複数行テキスト ボックスが改善され、余分な改行が挿入されなくなります。 これが望ましくない場合、アプリは、.NET Framework 4.0 をターゲットとする .NET Framework 4.5 で実行されているときに以前の動作を持つことができます。|
|スコープ|マイナー|
|Version|4.5|
|型|再ターゲット中|

