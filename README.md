# fc2ppvdb_ASVL 
-  fc2ppvdb Auto Search Video Links
- fc2ppvdb 自動搜尋影片連結


**fc2ppvdb_ASVL** 是專為 Google Chrome 瀏覽器及 Tampermonkey 插件設計的腳本工具。此腳本能夠自動在多個影片資源網站（例如 `_123av.com`、`missav.com`、`7mmtv.sx`、`javfc2.xyz`、`sukebei.nyaa.si` 和 `supjav.com`）中搜尋相關影片，並在頁面上自動生成快速跳轉按鈕。

---

## 功能特點

- **多站點支援**：
  - 自動搜尋以下影片資源網站：
    - `_123av.com`
    - `missav.com`
    - `7mmtv.sx`
    - `javfc2.xyz`
    - `sukebei.nyaa.si`
    - `supjav.com`
- **全自動搜尋**：
  - 根據 `fc2ppvdb` 網頁上的影片編號，自動搜尋多個站點的資源。
- **快速跳轉結果**：
  - 搜尋成功後，會在頁面上生成彩色按鈕，點擊即可於新標籤頁打開搜尋結果。
- **高性能與快取**：
  - 支援多站點並行搜尋（預設最多同時搜尋 3 個站點）。
  - 自動快取搜尋結果，提升效率，避免重複搜尋。
- **專屬 Google Chrome 支援**：
  - 專門針對 Google Chrome 瀏覽器及 Tampermonkey 插件進行優化，確保穩定性與流暢性。

---

## 安裝方法

### 第一步：安裝 Tampermonkey 插件

1. 打開 Google Chrome 瀏覽器。
2. 前往 [Tampermonkey 官方擴展頁面](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)。
3. 點擊 **「添加到 Chrome」** 按鈕，並完成安裝。

### 第二步：安裝腳本

1. 安裝完成 Tampermonkey 後，點擊瀏覽器右上角的 Tampermonkey 圖示。
2. 選擇 **「創建新腳本」**。
3. 將腳本代碼複製並貼到編輯器中。
4. 保存腳本，然後打開 **[fc2ppvdb.com](https://fc2ppvdb.com/)**，確認腳本是否正常執行。

---

## 使用方法

1. 打開 **[fc2ppvdb.com](https://fc2ppvdb.com/)**。
2. 腳本會自動掃描頁面上的影片編號。
3. 對於每個影片編號，腳本會在支援的站點中進行搜尋：
   - 如果找到結果，頁面上會生成一個彩色按鈕。
   - 點擊按鈕即可快速跳轉到對應站點的搜尋結果頁面。
4. 如果沒有結果，則不會生成按鈕。

---

## 支援站點

以下是目前支援的影片資源網站：

| 網站名稱            | 描述                     |
|---------------------|--------------------------|
| `_123av.com`        | 提供多種影片資源搜尋      |
| `missav.com`        | 包含大量影片詳細資訊      |
| `7mmtv.sx`          | 影片資源搜尋站點          |
| `javfc2.xyz`        | 專注於 FC2 影片搜尋       |
| `sukebei.nyaa.si`   | 種子資源搜尋平台          |
| `supjav.com`        | 提供 SupJav 搜尋支援      |

---

## 預設設定

腳本默認啟用了所有站點的搜尋功能，並發搜尋數量為 3。以下是預設設定：

```javascript
const defaultSettings = {
    enable_123av: true,     // 啟用 _123av 搜尋
    enableMissAV: true,     // 啟用 missav 搜尋
    enable7MMTV: true,      // 啟用 7mmtv 搜尋
    enableJAVFC2: true,     // 啟用 javfc2 搜尋
    enableSukebei: true,    // 啟用 sukebei 搜尋
    enableSupJav: true,     // 啟用 supjav 搜尋
    maxConcurrentSearches: 3, // 預設並行搜尋數量
};
