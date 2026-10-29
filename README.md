# Anode / Cathode Tamer 中文攻略

靜態攻略網站，適用 GitHub Pages。文字及參考資料來自 DigiKidult 整理，角色圖片使用本次提供的獨立精靈圖；基礎能力、敵人能力、道具價格及獎勵資料另按日本原版遊戲核對。

## 發佈

1. 將完整 ZIP 解壓，上傳所有檔案與 assets 資料夾至 GitHub 儲存庫根目錄。
2. Settings → Pages → Deploy from a branch，選擇分支及 / (root)。
3. 後續更新檔 ZIP 只需覆蓋同名檔案；保留既有 assets。

## 內容

- 數碼圖鑑：113 隻數碼獸，中日文名、能力及入手條件。
- 變數技：73 種組合、消耗與效果。
- 迷宮資料：18 個已命名迷宮，按輪次顯示敵人及初始能力、道具與金錢獎勵、版本比較。
- 新增數碼獸列為整個迷宮／任務完成後的獎勵，每個迷宮只顯示一次，並非每輪獲得。
- 頭目戰的敵人組合下方標示「迷宮中的頭目數碼獸無法捕捉。」；沒有獨立 Boss 區塊。
- 道具列表：50 件中日文道具及效果、16 件商店販售道具的買賣價、按版本列出的掉落迷宮與輪次。
- 數碼配章、廁所：初始獲得；數碼暴龍分析器：擊敗惡魔獸後取得。
- 隱藏關卡、配布 V 龍獸、版本資料及 DigiKidult 社交連結。

## 資料及限制

SP 為數值，不是百分比。卡片上的敵人能力為該輪初始值，未包含傷害或戰鬥效果。道具不保證每次掉落；首次攻略及特殊故事結算可能另有處理。隱藏關卡 D 第六、七輪仍待核對。原版數值讀取及部分程式已作隔離執行檢查，未完成全部遊戲流程實測。獨立程式測試不能用來推定獎勵每輪都會派發。

combat-stats.js / combat-stats.csv：敵人能力資料；rewards.js：獎勵表；items.js：道具與取得來源；dungeons.js：迷宮名稱及戰鬥組合。來源表及原始 ROM 未包含在發佈 ZIP 中。

## 本次更新

套用完整迷宮名稱對照；改正任務完成獎勵位置；頭目提示改為組合下方顯示；道具圖鑑改名為道具列表；加入三件初始／劇情道具的取得方式。道具取得來源及迷宮跳轉連結已同步更新。

### Variable-technique effect descriptions
Updated 72 technique descriptions from the original in-game explanations; Omegamon is intentionally unchanged. Replaced uncertain descriptions for 怪蛙王、大古加獸、砲彈獸, supplemented the verified stat-reset behavior for 怪蛙王 and 神龍獸, and labeled GranKuwagamon's value as the nominal first critical-check stage. Remaining duration and subsequent-roll uncertainties stay in detail notes. This update does not apply the separately pending tab renames, acquisition linking/version labels, or new learning-rule presentation.

### Variable-technique learning rules
Applied original-game learning rules from 61 recipe records to 71 techniques. Detail views show eligible learner/partner groups and the learner's known-tech prerequisite for higher techniques; group names link to catalogue profiles. Combination keywords search both original sheet terms and actual group members. The two techniques without native recipes are marked as special routes; observation-learning conditions are described separately, with no guarantee of learning after ten observations. Omegamon's effect text is unchanged. Other currently logged renames and acquisition cross-links are not included in this update.

### Method-specific acquisition and exchange-only sources
Added acquisition.js with capture-location candidates (excluding marked boss positions), whole-quest Server Room rewards, retained story/initial/distribution sources, and original exchange transformations. Each capture/reward link labels the applicable edition for that specific method; a limited route does not imply the entire species is unobtainable in the other edition. Catalogue profiles jump to the matching round or quest reward block, and stage cards already link back to catalogue profiles. 迷宮資料 is renamed 關卡攻略 while keeping #/dungeons unchanged. 交換限定 filtering covers 大便獸（鼻涕獸交換）、怪蛙獸（蝌蚪獸交換）、鬼魂獸（猛鬼獸交換）. Both original exchange selection routines were tested across all 113 species (226 cases). These three have no other source in the checked encounter/reward datasets; unresolved slots and unverified story routes are not invented. The separately logged 隱藏要素 tab rename remains pending.

### Consolidated acquisition display
Catalogue location/condition fields are now regenerated from 關卡攻略 encounter locations and quest rewards. Cards preview actual stage names, rounds and version labels; profiles expose all links and separate whole-quest completion conditions. Added acquisition-method filters and stage-name search. The original sheet location survives in sheetLocation for traceability. Known locations are not replaced with a generic pending warning; only capture success remains subject to in-game conditions. Rebuilding data also regenerates the acquisition view so older sheet locations do not overwrite the integration.

圖鑑收集清單：勾選狀態以網站專用鍵儲存在目前瀏覽器；可篩選已取得／未取得。清除網站資料或更換瀏覽器不會保留，無帳號同步。
關卡獎勵摘要：收合標題列出整個關卡的可能道具、任務完成新增數碼獸，以及三隻全部存活的額外獎勵；比較版本時分開顯示兩版。

2026-10-29：新增原版ROM屬性、地形、特殊特性與109項捕捉參考值；交換／配佈／任務取得不以0點捕捉表示。新增道具數值效果、回復上限與防禦晶片原版生效限制。兩版原版參數對照一致，原生道具應用352案例及復活32案例檢查通過。鋼鐵豆豆獸／南瓜獸VP按原版修正為6／8；奧米加獸整筆資料保持原樣。
