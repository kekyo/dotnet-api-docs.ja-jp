### <a name="httpruntimeappdomainapppath-throws-a-nullreferenceexception"></a>HttpRuntime.AppDomainAppPath は NullReferenceException をスローします。

|   |   |
|---|---|
|説明|ランタイムによってスローされる、.NET Framework 4.6.2、<code>T:System.NullReferenceException</code>取得するときに、 <code>P:System.Web.HttpRuntime.AppDomainAppPath</code> null 文字を含む値です。 .NET Framework 4.6.1 と以前のバージョンでは、ランタイムによってスローされる、<code>T:System.ArgumentNullException</code>です。|
|提案される解決策|この変更に応答する次のいずれかの操作を行うことができます。<ul><li>処理、<code>T:System.NullReferenceException</code>アプリケーションは、.NET Framework 4.6.2 で実行されている場合。</li><li>以前の動作を復元し、スローする .NET Framework 4.7 へのアップグレード、<code>T:System.ArgumentNullException</code>です。</li></ul>|
|スコープ|エッジ|
|Version|4.6.2|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Web.HttpRuntime.AppDomainAppPath?displayProperty=nameWithType></li></ul>|

