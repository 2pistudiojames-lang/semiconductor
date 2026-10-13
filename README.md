# 晶片製造所 — The Silicon Lab

半導體 3D 互動導覽網站，透過八個觀察站介紹晶片製造的概念。

## 本 repository 的範圍

**這是正式網站的部署版本快照，不是完整的開發原始碼專案。**

本次直接擷取目前 VPS 正在提供的靜態檔案，保留 HTML、已打包的 JavaScript/CSS、圖片、語音、背景音樂、gzip 預壓縮檔及 Three.js 授權文字。尚未取得原始 `src/`、建置設定、素材生成腳本或 source maps；不能宣稱可以從原始碼重建 bundle。

- 快照日期：2026-10-13（Asia/Taipei）
- 部署版本：`20260911T140931Z-bgm`
- 檔案與 SHA-256 清單：[`DEPLOYMENT-SNAPSHOT.json`](DEPLOYMENT-SNAPSHOT.json)
- 保留先前版本的 hashed assets 與音檔，與正式部署目錄一致，供已開啟的舊頁面使用。
- 不含 VPS 帳密、伺服器設定、TLS 私鑰、環境變數或其他專案資料。

## 本機預覽

不需 npm 安裝或建置。需 Python 3，以及支援 WebGL 的瀏覽器。

```bash
python3 -m http.server 4382 --bind 127.0.0.1
```

開啟 <http://127.0.0.1:4382/>。請使用 HTTP server，不要直接以 `file://` 開啟 ES module。若瀏覽器提示無法啟動 WebGL，請確認瀏覽器及 GPU 支援與硬體加速設定。

## 目錄

```text
index.html                   網站入口
static/                      已打包 JS、CSS 與圖片
assets/audio/                開場、八站旁白與背景音樂
THREE-LICENSE.txt            Three.js MIT 授權
DEPLOYMENT-SNAPSHOT.json     原部署檔案校驗清單
```

## 部署邊界

本 repository 不含自動部署 workflow。推送 GitHub 不會修改或重啟 VPS 網站。本次同步也沒有改動線上的 `/semi/`、VitaPlay 或其他服務。

## 授權

Three.js 的 MIT 授權見 `THREE-LICENSE.txt`。該第三方授權不代表本網站全部內容、音樂或素材都以 MIT 授權；本 repository 未額外宣告整站開源授權。
