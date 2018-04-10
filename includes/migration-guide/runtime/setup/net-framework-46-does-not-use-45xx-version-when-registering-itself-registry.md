### <a name="the-net-framework-46-does-not-use-a-45xx-version-when-registering-itself-in-the-registry"></a>.NET Framework 4.6 は、レジストリに登録する際に 4.5.x.x バージョンを使用しません。

|   |   |
|---|---|
|説明|いずれかが予想される場合があります、バージョン キーがレジストリに設定 (で<code>HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\NET Framework Setup\NDP\v4\Full</code>) .NET Framework 4.6 は、'4.6'、'4.5' で始まるためです。 4.6 は、新しいの可能なバージョン、リリース前 4.5.x と互換性があるいずれかを理解するには、どの .NET Framework のバージョンがコンピューターにインストールされている次のトピックにこれらのレジストリ キーに依存しているアプリを更新する必要があります。|
|提案される解決策|.NET Framework 4.5 のプローブ更新アプリケーションは、4.5 のレジストリ キーも 4.6 を使用するを検索してインストールされます。|
|スコープ|エッジ|
|Version|4.6|
|型|ランタイム|

