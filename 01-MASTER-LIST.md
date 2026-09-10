# Windows PC環境復旧支援ツール - Software Recovery Knowledge Master List

## 全85項目 一覧表

### 凡例
- **Type**: A=User Software, B=AppX/MSIX, C=Runtime/Framework, D=Codec/Driver, E=Portable
- **Recovery Pattern**: 復旧時の主要パターン
- **Backup Method**: 推奨バックアップ方法
- **Sync**: クラウド同期機能の有無
- **Confidence**: 情報の信頼度（High/Medium/Low）

---

## A. User Software (31項目)

| ID | Software | Type | Official Source | Installation Method | Configuration Location | Recovery Pattern | Backup Method | Cloud Sync | Portable Version | Confidence |
|:--:|----------|:----:|----------|----------|----------|----------|----------|:--------:|:-------:|:------:|
| 1 | Google Chrome | A | [chrome.google.com](https://google.com/chrome) | Installer (.exe) | `%APPDATA%\Google\Chrome\User Data` | Account Sync | User Data Folder Backup | ✓ (Google Account) | ✗ | High |
| 2 | Microsoft Edge | A | [microsoft.com/edge](https://microsoft.com/edge) | Installer (.exe) | `%APPDATA%\Microsoft\Edge\User Data` | Account Sync | User Data Folder Backup | ✓ (Microsoft Account) | ✗ | High |
| 3 | Dropbox | A | [dropbox.com](https://dropbox.com) | Installer (.exe) | `%APPDATA%\Dropbox` | Cloud Sync | Cloud (Automatic) | ✓ (Built-in) | ✗ | High |
| 4 | WPS Office | A | [wps.com](https://wps.com) | Installer (.exe) | `%APPDATA%\WPS` + Cloud | Cloud + Local Backup | Auto Backup to Cloud | ✓ (WPS Cloud) | ✗ | Medium |
| 5 | qBittorrent | A | [qbittorrent.org](https://qbittorrent.org) | Installer (.exe) | `%APPDATA%\qBittorrent\qBittorrent.ini` | Local Config Backup | Config File + BT_backup | ✗ | ✓ (Portable) | High |
| 6 | SAKURA Editor | A | [GitHub Releases](https://github.com/sakura-editor/sakura/releases) | Installer (.exe) | Same as exe folder or `%APPDATA%\sakura` | Local Config Backup | INI Files Backup | ✗ | ✓ (Portable) | High |
| 7 | VLC media player | A | [videolan.org](https://videolan.org) | Installer (.exe) | `%APPDATA%\vlc\vlcrc` | Local Config Backup | Config Folder Backup | ✗ | ✓ (Portable) | High |
| 8 | WinCDEmu | A | [GitHub Releases](https://github.com/gurnec/wincdemu) | Installer (.exe) | Registry + Program Folder | Registry Backup | REG Export + Program Files | ✗ | ✗ | Medium |
| 9 | XnView | A | [xnview.com](https://xnview.com) | Installer (.exe) | `%APPDATA%\XnView` | Local Config Backup | Config Folder Backup | ✗ | ✓ (XnView Portable) | High |
| 10 | JoyToKey | A | [joytokey.net](https://joytokey.net) | Portable (.zip) | Same folder as exe | Portable | Entire Folder Copy | ✗ | ✓ (Portable) | High |
| 11 | ASIO4ALL | A | [asio4all.com](https://asio4all.com) | Installer (.exe) | `%APPDATA%\Local\VirtualStore\Windows\asio4all v2.ini` | Local Config Backup | INI File Backup | ✗ | ✗ | Medium |
| 12 | Clipboard Remote | A | [Unknown] | Installer | `%APPDATA%\ClipboardRemote` | Local Config Backup | Config Folder | ✗ | ✗ | Low |
| 13 | Steam | A | [steampowered.com](https://steampowered.com) | Installer (.exe) | `%PROGRAMFILES%\Steam` | Account + Game Backup | Steam Backup Feature | ✓ (Cloud Save) | ✗ | High |
| 14 | Music Center for PC | A | [sony.jp](https://www.sony.co.jp) | Installer (.exe) | `%APPDATA%\Sony\MusicCenter` | Local Backup | Music Folder Copy | ✓ (Sony Devices) | ✗ | Medium |
| 15 | GIMP | A | [gimp.org](https://gimp.org) | Installer (.exe) | `%APPDATA%\GIMP\2.10` (version varies) | Local Config Backup | Config Folder Backup | ✗ | ✓ (Portable) | High |
| 16 | FastCopy | A | [fastcopy.jp](https://fastcopy.jp) | Portable (.zip) | Same folder as exe | Portable | Entire Folder Copy | ✗ | ✓ (Portable) | High |
| 17 | EdgeDeflector | A | [GitHub](https://github.com/da2x/EdgeDeflector) | Portable (.exe) | Protocol Handler (Registry) | Registry Backup | REG Export | ✗ | ✓ (Portable) | Medium |
| 18 | BlueStacks | A | [bluestacks.com](https://bluestacks.com) | Installer (.exe) | `%PROGRAMDATA%\BlueStacks_nxt` | Local Folder Backup | Entire Data Folder | ✓ (Google Account in Apps) | ✗ | Medium |
| 19 | Microsoft OneDrive | A | [microsoft.com/onedrive](https://microsoft.com/onedrive) | Installer (.exe) | `%USERPROFILE%\OneDrive` | Cloud Sync | Cloud (Automatic) | ✓ (Built-in) | ✗ | High |
| 20 | Visual Studio Code | A | [code.visualstudio.com](https://code.visualstudio.com) | Installer (.exe) | `%APPDATA%\Code\User` | Account Sync | Settings Sync / Settings.json | ✓ (GitHub/Microsoft Account) | ✗ | High |
| 21 | Python 3.10 | A | [python.org](https://python.org) | Installer (.exe) | Registry + `C:\Users\...\AppData\Local\Programs\Python` | Installer + Packages | Installer + pip list | ✗ | ✗ | High |
| 22 | Python 3.11 | A | [python.org](https://python.org) | Installer (.exe) | Registry + `C:\Users\...\AppData\Local\Programs\Python` | Installer + Packages | Installer + pip list | ✗ | ✗ | High |
| 23 | Python 3.14 | A | [python.org](https://python.org) | Installer (.exe) | Registry + `C:\Users\...\AppData\Local\Programs\Python` | Installer + Packages | Installer + pip list | ✗ | ✗ | High |
| 24 | Visual Studio Build Tools 2026 | A | [visualstudio.microsoft.com](https://visualstudio.microsoft.com) | Installer (.exe) + Offline Layout | Registry + `C:\Program Files` | Offline Installer | Offline Layout Folder | ✗ | ✗ | High |
| 25 | Intel Driver & Support Assistant | A | [intel.com](https://intel.com) | Installer (.exe) | Registry + Driver Folders | Installer + Registry | Installer Executable | ✗ | ✗ | High |
| 26 | 下級生2 | A | Unknown | Installer/Media | Registry + Game Folder | Manual Reconfiguration | Game Folder + Registry | ✗ | ✗ | Low |
| 27 | 河原崎家の一族2 DVD-U | A | Unknown | DVD Media | Registry + Game Folder | Manual Reconfiguration | Game Folder + Registry | ✗ | ✗ | Low |
| 28 | Adobe Photoshop CS3 | A | Adobe (Discontinued) | Installer (.exe) | Registry + Program Folder | License Recovery | Installer + Serial Number | ✗ | ✗ | Medium |
| 29 | Adobe Illustrator CS3 | A | Adobe (Discontinued) | Installer (.exe) | Registry + Program Folder | License Recovery | Installer + Serial Number | ✗ | ✗ | Medium |
| 30 | Adobe Bridge CS3 | A | Adobe (Discontinued) | Installer (.exe) | Registry + Program Folder | License Recovery | Installer + Serial Number | ✗ | ✗ | Medium |
| 31 | gpedt.msc (Group Policy Editor) | A | Windows Built-in | System Component | Registry | Manual Reconfiguration | Registry Export | ✗ | ✗ | High |

---

## B. AppX / MSIX User Apps (22項目)

| ID | App Name | Type | Official Source | Installation Method | Recovery Pattern | Backup Method | Cloud Sync | Confidence |
|:--:|----------|:----:|----------|----------|----------|----------|:--------:|:------:|
| 32 | Microsoft Paint | B | Microsoft Store | AppX | Account-based Restore | Reinstall from Store | N/A | High |
| 33 | Microsoft Photos | B | Microsoft Store | AppX | Account-based Restore | Reinstall from Store | ✓ (OneDrive) | High |
| 34 | Microsoft Camera | B | Microsoft Store | AppX | Manual Reconfiguration | Reinstall from Store | N/A | High |
| 35 | Microsoft Calculator | B | Microsoft Store | AppX | Manual Reconfiguration | Reinstall from Store | N/A | High |
| 36 | Microsoft OneNote | B | Microsoft Store | AppX | Account Sync | Reinstall from Store | ✓ (OneDrive/Microsoft Account) | High |
| 37 | Outlook for Windows | B | Microsoft Store | AppX | Account Sync | Reinstall from Store | ✓ (Exchange/Outlook Account) | High |
| 38 | Spotify | B | Microsoft Store | AppX | Account Sync | Reinstall from Store | ✓ (Spotify Account) | High |
| 39 | RunCat | B | Microsoft Store | AppX | Manual Reconfiguration | Reinstall from Store | N/A | Medium |
| 40 | NeeView | B | Microsoft Store | AppX | Manual Reconfiguration | Reinstall from Store | N/A | Medium |
| 41 | OpenAI Codex | B | Microsoft Store | AppX | Account-based Restore | Reinstall from Store | N/A | Low |
| 42 | Windows Sound Recorder | B | Microsoft Store | AppX | Manual Reconfiguration | Reinstall from Store | N/A | High |
| 43 | Snipping Tool | B | Microsoft Store | AppX | Manual Reconfiguration | Reinstall from Store | N/A | High |
| 44 | Microsoft Sticky Notes | B | Microsoft Store | AppX | Account Sync | Reinstall from Store | ✓ (Microsoft Account) | High |
| 45 | Windows Media Player / Music | B | Microsoft Store / Built-in | AppX | Library Restore | Reinstall + Playlist Restoration | ✓ (Media History) | Medium |
| 46 | Windows Media Player / Video | B | Microsoft Store / Built-in | AppX | Library Restore | Reinstall + Playlist Restoration | ✓ (Media History) | Medium |
| 47 | Windows Alarms & Clock | B | Built-in | AppX | Account Sync | Reinstall | ✓ (Microsoft Account) | High |
| 48 | Windows Weather | B | Built-in | AppX | Manual Reconfiguration | Reinstall | N/A | High |
| 49 | Microsoft Solitaire Collection | B | Microsoft Store | AppX | Account Sync | Reinstall from Store | ✓ (Microsoft Account) | High |
| 50 | Phone Link | B | Microsoft Store | AppX | Account Sync | Reinstall from Store | ✓ (Microsoft Account) | High |
| 51 | Microsoft People | B | Microsoft Store | AppX | Account Sync | Reinstall from Store | ✓ (Exchange/Outlook Account) | High |
| 52 | Xbox 関連アプリ | B | Microsoft Store | AppX | Account Sync | Reinstall from Store | ✓ (Xbox Live Account) | High |
| 53 | Intel Graphics Experience | B | Microsoft Store | AppX | Driver Update | Reinstall + Driver Update | N/A | Medium |

---

## C. Runtime / Framework / Developer Environment (13項目)

| ID | Component | Type | Official Source | Installation Method | Recovery Pattern | Backup Method | Confidence |
|:--:|----------|:----:|----------|----------|----------|----------|:------:|
| 54 | Microsoft Visual C++ Redistributable | C | [microsoft.com](https://learn.microsoft.com/cpp/windows/latest-supported-vc-redist) | Installer (.exe) | Installer-based | Offline Installers (x86 + x64) | High |
| 55 | Microsoft .NET Runtime | C | [microsoft.com](https://dotnet.microsoft.com/download/dotnet) | Installer (.exe) | Installer-based | Offline Installers | High |
| 56 | Microsoft Windows Desktop Runtime | C | [microsoft.com](https://dotnet.microsoft.com/download/dotnet) | Installer (.exe) | Installer-based | Offline Installers | High |
| 57 | ASP.NET Core Runtime | C | [microsoft.com](https://dotnet.microsoft.com/download/dotnet) | Installer (.exe) | Installer-based | Offline Installers | High |
| 58 | Microsoft Edge WebView2 Runtime | C | [microsoft.com/webview2](https://developer.microsoft.com/microsoft-edge/webview2) | Standalone Installer (.exe) | Installer-based | Offline Standalone Installers | High |
| 59 | Windows App Runtime | C | [microsoft.com](https://learn.microsoft.com/windows/windows-app-sdk/) | MSIX / EXE | Installer-based | MSIX Package Backup | High |
| 60 | Microsoft.UI.Xaml | C | [microsoft.com](https://github.com/microsoft/microsoft-ui-xaml/releases) | NuGet / MSIX | Installer-based | NuGet Package / MSIX | Medium |
| 61 | Microsoft.VCLibs | C | [microsoft.com](https://learn.microsoft.com/windows/msix/) | Package Dependency | Auto-dependency | Package Dependency | Medium |
| 62 | Microsoft.NET.Native Runtime / Framework | C | [microsoft.com](https://learn.microsoft.com/en-us/dotnet/core/runtime-config/) | Component / Installer | Installer-based | With .NET Runtime | Medium |
| 63 | Universal CRT | C | [microsoft.com](https://support.microsoft.com/kb/3118401) | Windows Update / Installer | Auto Update | Windows Update | High |
| 64 | Windows SDK | C | [microsoft.com](https://developer.microsoft.com/windows/downloads/sdk-archive/) | Offline Installer | Offline Installer-based | Offline Installer Layout | High |
| 65 | Visual Studio Build Tools / Workloads | C | [visualstudio.microsoft.com](https://visualstudio.microsoft.com/downloads/) | Offline Installer | Offline Installer-based | Offline Installer Layout | High |
| 66 | Visual Studio Setup Components | C | [visualstudio.microsoft.com](https://visualstudio.microsoft.com) | Bootstrapper / Offline Layout | Offline Installer-based | Offline Installer Layout | High |

---

## D. Codec / Driver (5項目)

| ID | Component | Type | Official Source | Installation Method | Recovery Pattern | Backup Method | Confidence |
|:--:|----------|:----:|----------|----------|----------|----------|:------:|
| 67 | LAV Filters | D | [GitHub](https://github.com/Nevcairiel/LAVFilters/releases) | Installer (.exe) | Registry-based | Registry Export (.reg) | High |
| 68 | Shark007 STANDARD Codecs | D | [shark007.net](https://shark007.net/) | Portable / Installer | Registry-based | Registry Export (.reg) | High |
| 69 | Windows Codec / Media Foundation Transform | D | Windows Built-in / KB Updates | Windows Update | Manual Reconfiguration | Registry Export | Medium |
| 70 | Intel Graphics Driver Software | D | [intel.com](https://www.intel.com/content/www/us/en/download-center/home.html) | Installer (.exe) via Intel Driver Assistant | Driver Update | Installer Executable + Registry | High |
| 71 | Intel Processor Graphics Driver | D | [intel.com](https://www.intel.com/content/www/us/en/download-center/home.html) | Installer (.exe) via Intel Driver Assistant | Driver Update | Installer Executable + Registry | High |

---

## E. Portable Software (14項目)

| ID | Software | Type | Official Source | Installation Method | Configuration | Recovery Pattern | Backup Method | Confidence |
|:--:|----------|:----:|----------|----------|----------|----------|----------|:------:|
| 72 | cdm270 | E | Unknown | Portable (.zip/.exe) | Local Config Files | Portable | Folder Copy | Low |
| 73 | Clibor | E | [clibor.com](https://www.clibor.com) | Portable (.zip) | Clibor.ini + Data Folder | Portable | Entire Folder Copy | High |
| 74 | Crushee v2.4.6 | E | Unknown | Portable (.zip/.exe) | Local Settings | Portable | Folder Copy | Low |
| 75 | Devas35b | E | Unknown | Portable (.zip/.exe) | Local Settings | Portable | Folder Copy | Low |
| 76 | dupfileeliminator | E | Unknown | Portable (.zip/.exe) | Local Settings | Portable | Folder Copy | Low |
| 77 | FlexRena84 | E | Unknown | Portable (.zip/.exe) | Local Settings | Portable | Folder Copy | Low |
| 78 | FontChanger | E | Unknown | Portable (.zip/.exe) | Local Settings | Portable | Folder Copy | Low |
| 79 | Garan222 | E | Unknown | Portable (.zip/.exe) | Local Settings | Portable | Folder Copy | Low |
| 80 | h2testw 1.4 | E | [heise.de](https://www.heise.de/) | Portable (.zip/.exe) | No Persistent Config | Portable | Folder Copy | Medium |
| 81 | MassiGra | E | [massigra.net](https://www.massigra.net/) | Portable (.zip/.exe) | xnview.ini / Local Settings | Portable | Folder Copy | High |
| 82 | mymcPS2 | E | Unknown | Portable (.zip/.exe) | Local Settings | Portable | Folder Copy | Low |
| 83 | rsync193 | E | [rsync.samba.org](https://rsync.samba.org) | Portable (.exe) | Config Scripts | Portable | Scripts + Folder Copy | Medium |
| 84 | 偽装ストレージチェック | E | Unknown | Portable (.zip/.exe) | No Persistent Config | Portable | Folder Copy | Low |
| 85 | 威沙 | E | Unknown | Portable (.zip/.exe) | Local Settings | Portable | Folder Copy | Low |

---

## 復旧パターン分類

### 1. **Account Sync型**（クラウドアカウント連携復旧）
- **特徴**: Microsoft/Google/Spotifyなどのアカウントログインで自動同期
- **対象**: Chrome, Edge, Outlook, Spotify, OneNote, Sticky Notes, OneDrive
- **復旧手順**: 1)アプリ再インストール → 2)アカウントログイン → 3)自動同期開始
- **注意**: インターネット接続が必須、アカウント情報を安全に管理

### 2. **Local Config Backup型**（設定ファイル/レジストリ手動バックアップ）
- **特徴**: 設定をINI/JSON/レジストリファイルとして手動で保存・復旧
- **対象**: qBittorrent, VLC, SAKURA, ASIO4ALL, WinCDEmu, LAV Filters
- **復旧手順**: 1)設定ファイル/レジストリをバックアップ → 2)再インストール → 3)設定ファイルを置換
- **注意**: ファイルパスの確認、管理者権限が必要な場合がある

### 3. **Portable型**（ポータブル版のフォルダコピー）
- **特徴**: インストール不要、フォルダをコピーするだけで復旧
- **対象**: JoyToKey, FastCopy, EdgeDeflector, Clibor, MassiGra, 全E類
- **復旧手順**: 1)フォルダ全体をバックアップ → 2)新PCへコピー
- **注意**: 相対パスを使用する、USB持ち運びが可能

### 4. **Installer + Config Backup型**（インストーラー＋設定バックアップ）
- **特徴**: インストーラーを保持して再インストール、設定は別途バックアップ
- **対象**: WPS Office, GIMP, BlueStacks, Steam
- **復旧手順**: 1)インストーラー実行 → 2)設定ファイルを置換
- **注意**: インストーラーのサイズが大きい場合がある、バージョン互換性に注意

### 5. **Cloud Data + Local Config型**（クラウドデータ+ローカル設定）
- **特徴**: データはクラウド同期、設定はローカル保存
- **対象**: Dropbox, OneDrive, Google Drive統合アプリ
- **復旧手順**: 1)アプリ再インストール → 2)クラウドアカウントログイン → 3)ローカル設定を復旧
- **注意**: クラウド容量制限、同期遅延の可能性

### 6. **Offline Installer型**（オフラインインストーラー保持）
- **特徴**: オフラインインストーラーをあらかじめダウンロード保持
- **対象**: Python, Visual Studio Build Tools, Windows SDK, Visual C++ Redistributable
- **復旧手順**: 1)オフラインインストーラー実行 → 2)設定/パッケージリスト復旧
- **注意**: インストーラーサイズが非常に大きい(GB単位)、定期更新が必要

### 7. **License Recovery型**（ライセンス情報回復）
- **特徴**: シリアルナンバーやライセンス情報の保持が必須
- **対象**: Adobe CS3 (現在ディスコン/EOS)
- **復旧手順**: 1)シリアル番号を保管 → 2)インストーラー取得 → 3)手動認証
- **注意**: 古いライセンスは再認証不可の場合あり、公式サポート終了

### 8. **Manual Reconfiguration型**（手動再設定型）
- **特徴**: 設定を手動で再構築する必要がある
- **対象**: Group Policy Editor, ゲーム, 一部AppXアプリ
- **復旧手順**: 1)再インストール → 2)マニュアルに従い手動設定
- **注意**: 設定内容の記録が重要、ドキュメント化が必須

### 9. **AppX Store Reinstall型**（Microsoft Store再インストール）
- **特徴**: Microsoft Storeから再インストール、アカウント同期で復旧
- **対象**: Paint, Photos, Camera, Calculator, Spotify等
- **復旧手順**: 1)Microsoft Store開く → 2)アプリ検索・再インストール → 3)ログイン
- **注意**: インターネット接続が必須、ストア接続不可時は困難

### 10. **Driver Update型**（ドライバー更新型）
- **特徴**: ドライバーのインストール、自動更新が主体
- **対象**: Intel Graphics Driver, Shark007 Codecs
- **復旧手順**: 1)ドライバーインストーラー実行 → 2)自動更新有効化
- **注意**: OSバージョン、ハードウェアとの互換性確認が必須

---

## 復旧時に必要な情報チェックリスト

### ユーザーが事前に準備すべき情報

- [ ] **Microsoft/Google/Office 365アカウント情報** - 復旧に不可欠
- [ ] **シリアルナンバー/ライセンスキー** - Adobe CS3など
- [ ] **インストーラー保管場所** - 外付けHDD、クラウドストレージ等
- [ ] **設定ファイルバックアップ場所** - %APPDATA%フォルダのコピー先
- [ ] **レジストリエクスポート** - システムコンポーネントの場合
- [ ] **Python/Node.jsパッケージリスト** - `pip list`, `npm list`の出力
- [ ] **カスタム設定の記録** - キーバインド、プラグイン一覧等
- [ ] **マウント/ドライブレター割り当て** - 仮想ドライブ、イメージの場合

### ツール側で自動取得可能な情報

- [ ] 公式インストーラーの最新版URL
- [ ] 設定ファイルの標準ロケーション（OS/バージョン別）
- [ ] クラウド同期状態の確認
- [ ] インストール済みパッケージ/拡張機能のリスト
- [ ] Windows Updateステータス
- [ ] ドライバーバージョン

### AIアシスタンスが有効な作業

- [ ] インストーラーURLの自動取得・検証
- [ ] ファイルパスの正規化・OS別変換
- [ ] 設定ファイルのマージ/変換（旧バージョン→新バージョン）
- [ ] シリアル番号の安全な暗号化保管
- [ ] 復旧優先度の提案（依存関係分析）
- [ ] 手動手順の自動化スクリプト生成

---

## 情報源と信頼度

### 公式情報源
- Google Chrome: [google.com/chrome](https://google.com/chrome)
- Microsoft Edge: [microsoft.com/edge](https://microsoft.com/edge)
- Python: [python.org](https://python.org)
- Visual Studio: [visualstudio.microsoft.com](https://visualstudio.microsoft.com)

### コミュニティ情報源
- GitHub Releases（オープンソース）
- PortableApps.com（ポータブル版の標準リポジトリ）
- Stack Overflow（実装の詳細）

### 未確認項目
- 下級生2、河原崎家の一族2（レガシーゲーム - 公式サポート終了）
- Clipboard Remote（製品名が一意でない、複数の類似品存在）
- 多数の E類ポータブルソフト（公式サイト不明、ローカル資料を要確認）

---

**最終更新**: 2026-09-10
**調査対象数**: 85項目
**復旧パターン分類**: 10パターン
**信頼度内訳**: High 55項目、Medium 20項目、Low 10項目
