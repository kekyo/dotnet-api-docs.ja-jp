### <a name="machinekeyencode-and-machinekeydecode-methods-are-now-obsolete"></a>MachineKey.Encode および MachineKey.Decode メソッドは、使用されなくなりました

|   |   |
|---|---|
|説明|これらのメソッドは今後使用しません。 これらのメソッドを呼び出すコードをコンパイルすると、コンパイラ警告が生成されます。|
|提案される解決策|別の方法として、<xref:System.Web.Security.MachineKey.Protect(System.Byte[],System.String[])> および <xref:System.Web.Security.MachineKey.Unprotect(System.Byte[],System.String[])> を使用することをお勧めします。 また、ビルド警告を抑制することができます、または古いコンパイラを使用してそれらを回避できます。 API は、まだサポートされています。|
|スコープ|マイナー|
|Version|4.5|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.Web.Security.MachineKey.Encode(System.Byte[],System.Web.Security.MachineKeyProtection)?displayProperty=nameWithType></li><li><xref:System.Web.Security.MachineKey.Decode(System.String,System.Web.Security.MachineKeyProtection)?displayProperty=nameWithType></li></ul>|

