# Anode / Cathode Tamer 中文攻略

以 DigiKidult《WS 數碼暴龍大冒險 陰／陽極訓練師 資料整合》的文字、地圖及參考圖片，配合本次提供的獨立精靈圖，重新編排的靜態攻略網站。

## 使用與發佈

本機可直接開啟 `index.html`，不需要安裝程式或 API 金鑰。

1. 將 ZIP 內全部檔案與 `assets` 資料夾上傳至 GitHub 儲存庫根目錄。
2. 前往 **Settings → Pages → Deploy from a branch**。
3. 選擇分支（通常是 `main`）及 **/ (root)**，然後 Save。
4. 等待 GitHub 完成發佈，開啟 Pages 顯示的網址。

全站使用相對資源路徑，可放在 GitHub 專案網址下。資料沒有即時連線依賴。往後提供的更新檔案 ZIP 只需覆蓋同名檔案，並維持資料夾結構。

## 內容

- 113 隻可操縱數碼獸，含中日文名、來源系列、入手條件與 DP / AP / PP / SP / VP / MP 基礎值。可按系列、版本限定、數值排序及搜尋。
- 73 種合體／臨時進化變數技，含組合、類型、VP 消耗及效果。提供組合關鍵字與攻擊／輔助篩選。
- 四個隱藏關卡及可放大的原表地圖。
- 限定配布 V 龍獸 ZERO、專屬技能及其與最後隱藏關卡的關係。
- 同梱版／活動限定版／彩色海外版、原表更新紀錄與相關攻略連結。
- 桌面導覽、手機選單、鍵盤搜尋快捷鍵 `/`、詳細資料對話框、DigiKidult 社交連結。

## 圖片與資料

來源：https://docs.google.com/spreadsheets/d/18_E3nXLaxxbro0q08IyX_u1SDZpNwQE8Qfc6jvSnAqw/edit

資料擷取日期：2026-10-24。原試算表未經修改。網站保留來源寫法、數值、空白地點及待確認效果；空白並不代表無法取得。原表在部分頁使用「機械邪龍獸／究極邪龍獸」不同名稱，相關頁面保留說明。配布數量及存檔存世估計屬原作者歷史資料，不是現時統計。

角色圖片只使用使用者提供的 `Downloads.zip`：`normal_000…112` 對應圖鑑 001…113；每隻兩個姿勢。`variable_000…072` 對應圖鑑 114…186。沒有採用原表三合一角色圖。地圖、歷史版本照片及示範截圖仍來自資料表，與角色精靈圖分開處理。

主要檔案：`index.html`、`base.css`、`style.css`、`app.js`、`data.js`、`icon.svg`、`.nojekyll` 與 `assets/`。開發及資料抽取檔不包含在發佈 ZIP。

資料、圖片整理歸原作者及提供者；Digimon 角色版權屬原權利人。本網站為非官方粉絲攻略。

## 迷宮資料更新

新增「迷宮資料」頁：原表列明的捕捉地點索引，以及日本原版陽極／陰極的遭遇配置。原版遭遇表每版 90 個內部區域索引、每區 4 組配置；未完成索引與迷宮／樓層名稱的對照，不能視為攻略順序，也不能由此推定捕捉條件或出現機率。資料不含修改版 ROM 的新增獎勵。

此次更新需一併覆蓋 index.html、app.js、style.css，並新增 dungeons.js、dungeon-ui.js。無需重新上傳圖片。

### 原版迷宮掃描
新增迷宮編號篩選、已核對的戰鬥槽對應及敵人 AP／PP 倍率。18 筆描述在兩版一致；184 個原生索引計算案例通過。迷宮 17 最後兩槽超出遭遇表宣告範圍，尚未列出敵人。編號未對照正式名稱，槽數不能直接當作實際樓層數。

## Dungeon grouping draft

- 18 collapsible dungeon sections; each contains its extracted battle slots.
- Supplied individual sprites link to existing profiles. Enemies without a matching catalogue entry retain their names; no substitute image is invented.
- Compare versions shows matching configuration numbers side by side and highlights species that differ in the corresponding enemy position. Mobile comparisons stack with version labels.
- Removed the separate 捕捉地點 view. Dungeon names and locations remain pending the user's draft.

### Boss entries
Dungeon sections now include a Boss overview using the first enemy marked by the original initialization code when the slot reaches the dungeon descriptor threshold. Marked battle cards are labeled. Both versions passed 552 isolated flag-calculation checks in total; this is not a complete boss playthrough. An unmarked descriptor is reported as no verified boss entry, never as proof of no boss.
