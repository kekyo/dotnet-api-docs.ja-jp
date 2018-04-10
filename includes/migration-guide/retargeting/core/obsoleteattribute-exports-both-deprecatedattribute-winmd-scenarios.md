### <a name="obsoleteattribute-exports-as-both-obsoleteattribute-and-deprecatedattribute-in-winmd-scenarios"></a>ObsoleteAttribute は、WinMD のシナリオで ObsoleteAttribute と DeprecatedAttribute の両方としてエクスポートします。

|   |   |
|---|---|
|説明|Windows メタデータ ライブラリ (.winmd ファイル) を作成するときに、<xref:System.ObsoleteAttribute?displayProperty=name>属性は両方としてエクスポート<xref:System.ObsoleteAttribute?displayProperty=name>と[Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute)です。|
|提案される解決策|使用する既存のソース コードの再コンパイル、 <xref:System.ObsoleteAttribute?displayProperty=name> C + からそのコードを使用するときに、属性が警告を生成する可能性があります +/CX または JavaScript.We 両方を適用することはお勧めしません<xref:System.ObsoleteAttribute?displayProperty=name>と[Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute)マネージ アセンブリ内のコードのビルド警告が生成する可能性があります。|
|スコープ|エッジ|
|Version|4.5.1|
|型|再ターゲット中|

