# **fc2ppvdb_ASVL**
- **fc2ppvdb Auto Search Video Links**
- **fc2ppvdb 自動搜尋影片連結**

**fc2ppvdb_ASVL** 是一款專為 **Google Chrome 瀏覽器** 和 **Violentmonkey/Tampermonkey 插件** 設計的用戶腳本工具。此腳本可以自動在多個影片資源網站（例如 `_123av.com`、`missav.com`、`7mmtv.sx`、`javfc2.xyz`、`sukebei.nyaa.si` 和 `supjav.com`）中搜尋相關影片，並在頁面上生成快速跳轉按鈕，提升用戶搜尋效率。

---

## **功能特點**

- **多站點支援**：
  - 自動搜尋以下影片資源網站：
    - `_123av.com`
    - `missav.com`
    - `7mmtv.sx`
    - `javfc2.xyz`
    - `sukebei.nyaa.si`
    - `supjav.com`
    - `3xplanet.com`
- **全自動搜尋**：
  - 根據 **fc2ppvdb** 網頁上的影片編號，自動搜尋多個站點的影片資源。
- **快速跳轉結果**：
  - 搜尋成功後，會在頁面上生成可點擊的彩色按鈕，點擊即可於新標籤頁打開搜尋結果。
- **高性能與快取**：
  - 自動快取搜尋結果（快取時間默認為 12 小時），提升效率並減少重複請求。
- **專屬 Google Chrome/Violentmonkey 支援**：
  - 專為 Google Chrome 及 **Violentmonkey** 插件進行優化，確保穩定性與流暢性。

---

## **安裝方法**

### **第一步：安裝用戶腳本管理器**

1. 打開 Google Chrome 或其他支持的瀏覽器。
2. 安裝以下任一用戶腳本管理器：
   - [Violentmonkey](https://violentmonkey.github.io/)（推薦，支持完整功能）
   - [Tampermonkey](https://www.tampermonkey.net/)（部分功能可能受限制）

3. 點擊 **「添加到瀏覽器」** 按鈕，並完成安裝。

---

### **第二步：安裝腳本**

1. 安裝完成用戶腳本管理器後
2. 手動安裝，選擇用戶腳本管理器的 **「創建新腳本」** 功能。
3. 將腳本代碼複製並貼到編輯器中。
4. 保存腳本，然後打開 **[fc2ppvdb.com](https://fc2ppvdb.com/)** 確認腳本是否正常執行。

---

## **使用方法**

1. 打開 **[fc2ppvdb.com](https://fc2ppvdb.com/)**。
2. 當頁面加載完成後，腳本會自動掃描頁面上的影片編號。
3. 對於每個影片編號，腳本會在支援的站點中進行搜尋：
   - 如果找到結果，頁面上會生成一個彩色按鈕。
   - 按鈕顯示站點名稱，點擊即可快速跳轉到對應站點的搜尋結果頁面。
4. 如果沒有結果，則不會生成按鈕。

---

## **支援站點**

以下是目前支援的影片資源網站列表：

| **網站名稱**         | **描述**                      |
|---------------------|------------------------------|
| `_123av.com`        | 提供多語言支持的影片資源搜尋   |
| `missav.com`        | 包含詳細影片信息的高質量站點   |
| `7mmtv.sx`          | 支援多分類影片資源的搜尋站點   |
| `javfc2.xyz`        | 專注於 FC2 影片的搜索引擎      |
| `sukebei.nyaa.si`   | 提供成人內容的 BT 資源搜索引擎 |
| `supjav.com`        | 成人視頻搜索引擎，支持多種分類 |
| `3xplanet.com`      | 集合多種成人資源的搜索網站     |

---

## **配置選項**

### **1. 最大並行搜索數量**
每個站點的最大並行搜索數量默認為 3，可以在腳本內調整：
```javascript
new Site(name, searchUrlFunc, responseHandler, buttonColor, queryInterval, maxConcurrentSearches);
