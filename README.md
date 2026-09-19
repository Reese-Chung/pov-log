# 我的觀點紀錄 — PWA 版

一個記錄電影、書籍、美食與日常的個人紀錄本。可安裝到手機主畫面、離線使用，資料存在自己的瀏覽器裡。

## 檔案說明

| 檔案 | 用途 |
|---|---|
| `index.html` | 整個 app，介面與功能都在這一個檔案裡 |
| `manifest.webmanifest` | app 名稱、圖示、啟動方式的設定 |
| `sw.js` | 離線功能，把檔案快取在裝置上 |
| `icon-192.png` / `icon-512.png` | app 圖示 |
| `icon-512-maskable.png` | Android 自動裁切用的圖示 |
| `apple-touch-icon.png` | iPhone 主畫面圖示 |

七個檔案必須放在同一層資料夾，不要分資料夾放。

## 部署到 GitHub Pages

1. 註冊並登入 GitHub。
2. 點右上角「＋」→「New repository」。Repository name 填 `pov-log`，選 **Public**，按「Create repository」。
3. 在新頁面點「uploading an existing file」，把上述七個檔案一起拖進去，按「Commit changes」。
4. 進入 repository 的「Settings」→ 左側「Pages」。
5. Source 選「Deploy from a branch」，Branch 選 `main`、資料夾選 `/ (root)`，按「Save」。
6. 等待約一到三分鐘，重新整理該頁面，上方會出現網址，格式為 `https://你的帳號.github.io/pov-log/`。

必須使用 https 網址，離線與安裝功能才會生效。用電腦直接雙擊開啟 `index.html` 只能當一般網頁使用。

## 安裝到手機

- **iPhone**：用 Safari 開啟網址，點下方「分享」→「加入主畫面」。必須是 Safari，Chrome 不支援。
- **Android**：用 Chrome 開啟網址，點右上角選單→「安裝應用程式」或「加到主畫面」。
- **電腦**：Chrome 或 Edge 網址列右側會出現安裝圖示。

## 搬移既有紀錄

瀏覽器資料依網址分開存放，舊網址的紀錄不會自動搬過來。

1. 在舊頁面點「備份」→「下載備份檔」或「複製備份文字」。
2. 在新網址點「備份」→ 選擇備份檔，或貼上備份文字後按「匯入貼上的文字」。

## 日後更新

把新版的 `index.html` 上傳覆蓋即可。`sw.js` 開頭的 `VERSION` 改成 `v2`、`v3`，可確保使用者拿到新版而不是舊的快取。使用者的紀錄不會因更新而消失。

## 資料與備份

紀錄存在各自裝置的瀏覽器中，不會上傳到任何伺服器。以下情況會遺失資料：清除瀏覽器資料、使用無痕模式、iPhone 長期未開啟該網站。建議每隔一段時間匯出一次備份，存到雲端硬碟。
