### <a name="data-written-to-printsystemjobinfojobstream-must-be-in-xps-format"></a>PrintSystemJobInfo.JobStream に書き込まれたデータは XPS 形式である必要があります。

|   |   |
|---|---|
|説明|<xref:System.Printing.PrintSystemJobInfo.JobStream>プロパティは、印刷ジョブのストリームを公開します。 ユーザーは、このストリームに書き込むことによって、基になるオペレーティング システムの印刷コンポーネントに生データを送信できます。Windows 8 および Windows オペレーティング システムの以降のバージョンの .NET Framework 4.5 以降、このストリームに書き込まれたデータする必要があります XPS 形式のパッケージ ストリームにします。|
|提案される解決策|印刷内容を出力するには、次のいずれかの操作を行います。<ul><li><xref:System.Windows.Xps.XpsDocumentWriter> クラスを使用して印刷内容を出力します。 これが、推奨される方法です。</li><li>によって返されるストリームに送信するデータを確認してください、<xref:System.Printing.PrintSystemJobInfo.JobStream>プロパティは、XPS 形式のパッケージ ストリームにします。</li></ul>|
|スコープ|マイナー|
|Version|4.5|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Printing.PrintSystemJobInfo.JobStream?displayProperty=nameWithType></li></ul>|

