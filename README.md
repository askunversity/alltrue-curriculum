# Alltrue Curriculum

Google Apps Script 課表與點名系統。

## 專案檔案

- `core.gs.txt`：主程式，包含課表管理、點名單產生、回寫、獎金計算、衝突報告。
- `Sidebar_DateRange.html`：產生點名單的日期區間側邊欄。
- `Sidebar_MonthPicker.html`：月份匯出與月統計側邊欄。

## 目前版本

- 版本：`v2.1`
- 更新日期：`2026/03/03`
- 本次重點：取消學生欄位限制，學生欄有值就抓。

## 使用方式

1. 將 `core.gs.txt` 內容貼到 Google Apps Script 專案主檔。
2. 將 `Sidebar_DateRange.html` 與 `Sidebar_MonthPicker.html` 建立為 HTML 檔。
3. 重新整理試算表，讓 `onOpen()` 重新建立選單。

## 版本更新紀律

每次更新請同步完成以下事項：

1. 修改 `core.gs.txt` 檔頭版本號與更新日期。
2. 更新 `showVersionInfo()` 內的版本號、日期與本次重點。
3. 在本 README 的「目前版本」區塊更新版本、日期、重點。
4. 在 `CHANGELOG.md` 新增一筆本次修改描述，至少寫清楚日期、版本、重點。
5. 準備 commit 前，先整理一段「本次修改描述」，內容要能直接對應 commit message。
6. 在 Git commit message 清楚描述本次變更，例如：
   - `feat: remove student cell restrictions`
   - `fix: improve attendance write-back conflict reporting`
   - `chore: update version info to v2.1`

## 建議規範

- 功能變更先改程式，再改版本資訊。
- 影響使用者行為的調整要寫進 `showVersionInfo()`。
- 準備 commit 時，要同時整理「修改摘要」與「commit message」，避免只有改程式沒有留下說明。
- 只有確認點名單、回寫或報表流程正常後再推送到 GitHub。
