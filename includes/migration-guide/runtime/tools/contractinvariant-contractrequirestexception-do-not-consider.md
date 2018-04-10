### <a name="contractinvariant-or-contractrequirestexception-do-not-consider-stringisnullorempty-to-be-pure"></a>Contract.Invariant または Contract.Requires<TException>純粋に String.IsNullOrEmpty は考慮されません

|   |   |
|---|---|
|説明|固定コントラクトの場合は、.NET Framework 4.6.1 を対象とするアプリの<xref:System.Diagnostics.Contracts.Contract.Invariant%2A?displayProperty=nameWithType>または前提条件のコントラクトを<xref:System.Diagnostics.Contracts.Contract.Requires%2A?displayProperty=nameWithType)>呼び出し、<xref:System.String.IsNullOrEmpty%2A?displayProperty=nameWithType>メソッド、リライター出力コンパイラの警告 CC1036:&quot;メソッドへの呼び出しを検出しました 'System.String.IsNullOrWhteSpace(System.String)' [単純] せずメソッドにします。&quot;これは、コンパイラの警告はコンパイラ エラーではなくです。|
|提案される解決策|この動作については [GitHubの問題 #339](https://github.com/Microsoft/CodeContracts/issues/339) で報告されています。 この警告をなくすため、ダウンロードしてから、コード コントラクト ツールのソース コードの更新バージョンをコンパイル[GitHub](https://github.com/Microsoft/CodeContracts/blob/master/README.md)です。 ページ下部から情報をダウンロードできます。|
|スコープ|マイナー|
|Version|4.6.1|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Diagnostics.Contracts.Contract.Invariant(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Contracts.Contract.Requires(System.Boolean)?displayProperty=nameWithType></li></ul>|

