### <a name="managed-browser-hosting-controls-from-the-net-framework-11-and-20-are-blocked"></a>.NET Framework 1.1 および 2.0 からホスト コントロールを管理対象ブラウザーはブロックします。

|   |   |
|---|---|
|説明|これらのコントロールのホストは、Internet Explorer でブロックされます。|
|提案される解決策|Internet Explorer では、マネージ ブラウザーを使用してコントロールをホストするアプリケーションは起動できません。 レジストリ サブキーの EnableIEHosting 値を設定して、以前の動作を復元することができます<code>HKLM/SOFTWARE/MICROSOFT/.NETFramework</code>に<code>1</code>x86 システムおよび x64 での 32 ビット プロセスのシステムを設定したり、 <code>EnableIEHosting</code> のレジストリサブキーの値<code>HKLM/SOFTWARE/Wow6432Node/Microsoft/.NETFramework</code>に<code>1</code>x64 の 64 ビット プロセス用のシステムです。|
|スコープ|マイナー|
|Version|4.5|
|型|ランタイム|

