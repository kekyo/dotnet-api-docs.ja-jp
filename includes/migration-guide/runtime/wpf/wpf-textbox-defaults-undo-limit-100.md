### <a name="wpf-textbox-defaults-to-undo-limit-of-100"></a><span data-ttu-id="20da1-101">WPF の TextBox の既定値は 100 の制限値を元に戻す</span><span class="sxs-lookup"><span data-stu-id="20da1-101">WPF TextBox defaults to undo limit of 100</span></span>

|   |   |
|---|---|
|<span data-ttu-id="20da1-102">説明</span><span class="sxs-lookup"><span data-stu-id="20da1-102">Details</span></span>|<span data-ttu-id="20da1-103">.NET 4.5 では、WPF テキスト ボックスの既定の元に戻す上限は 100 です (.NET 4.0 では無制限でした)。</span><span class="sxs-lookup"><span data-stu-id="20da1-103">In .NET 4.5, the default undo limit for a WPF textbox is 100 (as opposed to being unlimited in .NET 4.0)</span></span>|
|<span data-ttu-id="20da1-104">提案される解決策</span><span class="sxs-lookup"><span data-stu-id="20da1-104">Suggestion</span></span>|<span data-ttu-id="20da1-105">制限を明示的に設定することができます、元に戻す制限の 100 が低すぎる場合は、 <xref:System.Windows.Controls.Primitives.TextBoxBase.UndoLimit></span><span class="sxs-lookup"><span data-stu-id="20da1-105">If an undo limit of 100 is too low, the limit can be set explicitly with <xref:System.Windows.Controls.Primitives.TextBoxBase.UndoLimit></span></span>|
|<span data-ttu-id="20da1-106">スコープ</span><span class="sxs-lookup"><span data-stu-id="20da1-106">Scope</span></span>|<span data-ttu-id="20da1-107">エッジ</span><span class="sxs-lookup"><span data-stu-id="20da1-107">Edge</span></span>|
|<span data-ttu-id="20da1-108">Version</span><span class="sxs-lookup"><span data-stu-id="20da1-108">Version</span></span>|<span data-ttu-id="20da1-109">4.5</span><span class="sxs-lookup"><span data-stu-id="20da1-109">4.5</span></span>|
|<span data-ttu-id="20da1-110">型</span><span class="sxs-lookup"><span data-stu-id="20da1-110">Type</span></span>|<span data-ttu-id="20da1-111">ランタイム</span><span class="sxs-lookup"><span data-stu-id="20da1-111">Runtime</span></span>|
|<span data-ttu-id="20da1-112">影響を受ける API</span><span class="sxs-lookup"><span data-stu-id="20da1-112">Affected APIs</span></span>|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

