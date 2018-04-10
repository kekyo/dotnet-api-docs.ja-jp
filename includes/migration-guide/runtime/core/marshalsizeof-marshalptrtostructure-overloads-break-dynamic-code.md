### <a name="marshalsizeof-and-marshalptrtostructure-overloads-break-dynamic-code"></a>Marshal.SizeOf および Marshal.PtrToStructure オーバー ロードは、動的なコードを中断します。

|   |   |
|---|---|
|説明|以降では、.NET Framework 4.5.1、メソッドに動的に結びつける<xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601>、 <xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601(%60%600)>、 <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Object)>、 <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Type)>、 <xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr)>、または<xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr,%60%600)>、(を使用して Windows PowerShell、IronPython、または例については、dynamic キーワード (C#))つながる<code>MethodInvocationExceptions</code>できる可能性のあるスクリプト エンジンにあいまいなこれらのメソッドの新しいオーバー ロードが追加されているためです。|
|提案される解決策|どのオーバー ロードを明確に示す、更新スクリプトを使用する必要があります。 これは、一般に、メソッドの型パラメーターを <xref:System.Type> として明示的にキャストすることによって行われます。 この問題の回避方法の詳細と例については、[このリンク](https://support.microsoft.com/kb/2909958/) を参照してください。|
|スコープ|マイナー|
|Version|4.5.1|
|型|ランタイム|

