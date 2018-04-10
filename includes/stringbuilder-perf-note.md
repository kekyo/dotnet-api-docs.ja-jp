文字ベースのインデックスを使用して、<xref:System.Text.StringBuilder.Chars%2A>プロパティは、次の条件下で非常に低速であることができます。

- <xref:System.Text.StringBuilder>インスタンスが大きい (たとえば、含まれています数万文字)。
- <xref:System.Text.StringBuilder>は"chunky"なです。 つまりなどメソッドへの呼び出しを繰り返す<xref:System.Text.StringBuilder.Append%2A?displayProperty=nameWithType>オブジェクトの拡張に自動的に<xref:System.Text.StringBuilder.Capacity%2A?displayProperty=nameWithType>プロパティと、メモリの割り当てられた新しいチャンクです。

各文字のアクセスは、リンク リスト全体にインデックスを適切なバッファーを検索するチャンクのため、パフォーマンスが著しく低下します。

> [!NOTE]
>  大規模なであっても"chunky な"<xref:System.Text.StringBuilder>オブジェクトを使用して、<xref:System.Text.StringBuilder.Chars%2A>プロパティを 1 つまたは少数の文字インデックス ベースのアクセスをごくわずかでありのパフォーマンスに影響は通常、これは、 **0 (n)**操作します。 内の文字を反復処理するときに、パフォーマンスに大きな影響が発生、<xref:System.Text.StringBuilder>オブジェクトは、 **O(n^2)**操作します。 

文字ベースのインデックスを使用してパフォーマンスの問題が発生した場合<xref:System.Text.StringBuilder>オブジェクトを次の回避策のいずれかを使用することができます。

- 変換、<xref:System.Text.StringBuilder>インスタンスを<xref:System.String>を呼び出して、<xref:System.Text.StringBuilder.ToString%2A>メソッドを文字列内の文字にアクセスします。

- 既存の内容をコピー<xref:System.Text.StringBuilder>を新しいオブジェクトが事前にサイズ設定<xref:System.Text.StringBuilder>オブジェクト。 パフォーマンス向上のため、新しい<xref:System.Text.StringBuilder>chunky なオブジェクトではありません。 例:

   ```csharp
   // sbOriginal is the existing StringBuilder object
   var sbNew = new StringBuilder(sbOriginal.ToString(), sbOriginal.Length);
   ```
   ```vb
   ' sbOriginal is the existing StringBuilder object
   Dim sbNew = New StringBuilder(sbOriginal.ToString(), sbOriginal.Length)
   ```
- 初期容量の設定、<xref:System.Text.StringBuilder>は呼び出すことによって、最大の予想サイズにほぼ等しいを値にオブジェクト、<xref:System.Text.StringBuilder.%23ctor(System.Int32)>コンス トラクターです。 場合であってもメモリ全体のブロックを割り当てますこのことに注意してください、<xref:System.Text.StringBuilder>ほとんど処理能力の上限に到達します。
