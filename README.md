# Battery Parking Lab｜互動電池充電科學教學

用 Elon Musk 提過的「停車場找車位」比喻，引導使用者理解為什麼手機、電動車充電接近滿電時經常變慢。再延伸解釋鋰離子電池典型的 CC/CV 充電、溫度保護與充電曲線。

## 功能
- 100 格互動停車場，拖曳 0–100% 電量滑桿
- 動畫播放／暫停、跳至指定電量
- 電動車／手機切換
- 電池溫度情境、相對充電功率曲線、充電時間比較
- 科學原理與小測驗
- 手機及桌面版響應式設計

> 教學內容為簡化示意；模擬曲線與相對充電功率不是實車／實機量測，也不是特定品牌的測試結果。不同電芯、充電器與 BMS 策略差異很大；80% 並非通用轉折點。

## 直接使用
將 `index.html` 用瀏覽器開啟即可。介面字型使用 Google Fonts，離線時會自動使用系統字型；主要互動功能不需要網路。

## GitHub Pages 發布設定（GitHub 帳號：Vujad）
1. 儲存庫已建立：`https://github.com/Vujad/battery-parking-lab`。
2. 確認 `index.html`、`.nojekyll`、`README.md` 位於 repository 根目錄的 `main` 分支。
3. 前往 repository **Settings → Pages**，在 **Build and deployment → Source** 選 **Deploy from a branch**。
4. Branch 選 `main`、資料夾選 `/(root)`，然後 Save。
5. 部署完成後，到 Settings → Pages 點 **Visit site**。一般專案網站網址格式：`https://<你的 GitHub 帳號>.github.io/battery-parking-lab/`。
6. 若希望放到個人檔案展示：打開 GitHub 個人頁面，將該 repository **Pin**（釘選），並在個人 Profile README 或個人網站加上公開網址。

### 更新網站
更新 `index.html` 並推送到所選分支，即會觸發重新發布。

### 公開前確認
- 網站內容及 repository 的所有公開檔案都可能被他人看到、複製與分享。
- 不要上傳帳號密碼、API key、個資或敏感資料。
- 公開不等於自動有人瀏覽；搜尋引擎收錄及分享流量並不保證。
- GitHub Pages 提供網站託管，不會自動建立獨立網域、訂閱系統、後端資料庫或流量分析。

GitHub 官方指引：https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## 放進個人作品集可以怎麼介紹
**專案名稱：** Battery Parking Lab — 充電科學互動教學網站

**專案摘要：** 以生活化比喻與即時互動可視化，將抽象的鋰離子充電原理轉化為人人能操作的教學體驗。使用原生 HTML、CSS 與 JavaScript 實作，涵蓋狀態驅動動畫、響應式介面與互動式知識檢核。

**價值：** 展示把複雜概念轉化為可理解、可驗證、可分享的數位產品能力；可作為技術教育、科普分享與 UI/UX 作品。

## Cloudflare Pages 同步部署（建議：連接 GitHub）
1. 先在 GitHub 建立 `Vujad/battery-parking-lab` 公開儲存庫，將本目錄的 `index.html`、`README.md`、`.nojekyll` 上傳至 `main` 分支根目錄。
2. 到 Cloudflare Dashboard → Workers & Pages → Create application → Pages → Connect to Git，授權 Cloudflare 存取該儲存庫。
3. 選 `Vujad/battery-parking-lab`，專案名稱 `battery-parking-lab`。
4. Production branch=`main`；Framework preset=`None`；Build command 留空（如 UI 要求則填 `exit 0`）；Build output directory=`.`。
5. 儲存並部署。Cloudflare Pages 成功後會顯示 `https://battery-parking-lab.pages.dev/` 或因命名衝突而調整的網域。實際網址以 Cloudflare 控制台為準。
6. GitHub Repo Settings → Pages → Deploy from a branch → `main` → `/(root)` → Save。成功後網站通常位於 `https://vujad.github.io/battery-parking-lab/`。
7. 之後只要更新 `main` 分支的 `index.html`，GitHub Pages 與 Cloudflare Pages 都會重新部署。

> **注意：** Cloudflare Pages 新專案不要先選 Direct Upload，若想從 GitHub 自動部署。使用 Direct Upload 建立的專案無法改為 Git integration，須另建新專案。

> 部署是否完成，請以 GitHub Pages 與 Cloudflare Pages 的發布狀態及實際可存取的網址為準。