### <a name="incorrect-code-generation-when-passing-and-comparing-uint16-values"></a>不適切なコード生成を渡すと UInt16 値を比較します。

|   |   |
|---|---|
|説明|.NET Framework 4.7 で導入された、変更のため場合によっては正しく実行されていない .NET Framework 4.7 上のアプリケーションで JIT コンパイラによって生成されたコードを比較して 2 つ<code>T:System.UInt16</code>値。 詳細については、次を参照してください。[問題 #11508: サイレントの不適切な codegen を渡すと、ushort args を比較するときに](https://github.com/dotnet/coreclr/issues/11508)GitHub.com にします。|
|提案される解決策|.NET Framework 4.7 に 16 ビット符号なしの値の比較に問題が発生する場合、は、.NET Framework 4.7.1 にアップグレードします。|
|スコープ|エッジ|
|Version|4.7|
|型|ランタイム|

