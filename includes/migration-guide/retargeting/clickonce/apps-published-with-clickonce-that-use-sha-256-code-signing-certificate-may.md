### <a name="apps-published-with-clickonce-that-use-a-sha-256-code-signing-certificate-may-fail-on-windows-2003"></a>Windows 2003 で sha-256 コード署名証明書を使用する ClickOnce で発行されたアプリが失敗します。

|   |   |
|---|---|
|説明|この実行可能ファイルは SHA256 で署名されます。 以前は、コード署名証明書が SHA-1 か SHA-256 に関係なく、SHA 1 で署名されました。 この方法は、次の対象に適用されます。<ul><li>Visual Studio 2012 以降でビルドされたすべてのアプリケーション。</li><li>.NET Framework 4.5 がインストールされているシステム上で、Visual Studio 2010 以前でビルドされたアプリケーション。</li></ul>さらに、.NET Framework 4.5 以降が存在する場合、コンパイル対象となった .NET Framework のバージョンに関係なく、ClickOnce マニフェストはSHA-256 証明書の SHA 256 で署名されます。|
|提案される解決策|ClickOnce 実行可能ファイルの署名の変更に影響を与える Windows Server 2003 システムのみです。これらは、サポート技術情報 938397 がインストールされている必要があります。アプリが .NET Framework 4.0 またはそれ以前のバージョンをターゲットしている場合でも SHA 256 でマニフェストに署名の変更には、.NET Framework 4.5 以降のバージョンに対するランタイム依存関係が導入されています。|
|スコープ|エッジ|
|Version|4.5|
|型|再ターゲット中|

