**fc2ppvdb_ASVL**
- **fc2ppvdb Auto Search Video Links**
- **fc2ppvdb 自動搜尋影片連結**

**fc2ppvdb_ASVL** 是一款專為 **Google Chrome 瀏覽器** 和 **Violentmonkey/Tampermonkey 插件** 設計的用戶腳本工具。此腳本可以自動在多個影片資源網站（例如 `_123av.com`、`missav.ws`、`7mmtv.sx`、`javfc2.xyz`、`sukebei.nyaa.si` 和 `supjav.com`）中搜尋相關影片，並在頁面上生成快速跳轉按鈕，提升用戶搜尋效率。

---

## **功能特點**

- **多站點支援**：
  - 自動搜尋以下影片資源網站：
    - `_123av.com`
    - `missav.ws`
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

# **安裝方法**

本指南將引導您如何安裝用戶腳本管理器（如 Violentmonkey 或 Tampermonkey）並啟用開發者模式，最後完成腳本的安裝。

---

## **第一步：安裝用戶腳本管理器**

1. 打開 Google Chrome 或其他支持的瀏覽器。
2. 安裝以下任一用戶腳本管理器：
   - [Violentmonkey](https://violentmonkey.github.io/)（推薦，支持完整功能）
   - [Tampermonkey](https://www.tampermonkey.net/)（部分功能可能受限制）
3. 點擊 **「添加到瀏覽器」** 按鈕，並完成安裝。

---

## **第二步：啟用開發者模式**

以下是啟用開發者模式的詳細步驟：

### **1. 打開 Chrome 設定選單**

點擊右上角三個點的 **「設定」** 按鈕：

![設定](https://github.com/user-attachments/assets/fd856da3-da4f-4b8f-a6f6-8b693edaeddc)

---

### **2. 選擇「擴展程序」**

在設定選單中，選擇 **「設定」**：

![擴展程序](https://github.com/user-attachments/assets/10865530-d2b2-453b-9ee7-53ea80fc5f2a)

---

### **3. 進入擴展程序頁面**

進入擴展程序頁面後，您會看到所有已安裝的擴展程序列表：

![擴展程序頁面](https://github.com/user-attachments/assets/4284a97a-36ae-4908-a853-d0e6efdc7b03)

---

### **4. 啟用開發者模式**

在頁面右上角，打開 **「開發者模式」** 開關：

![開發者模式](https://github.com/user-attachments/assets/b8e91da8-a2e7-48f2-9013-9f5ab162ed80)

---

## **第三步：安裝腳本**

1. 安裝完成用戶腳本管理器後，啟動腳本安裝過程。
2. 手動安裝腳本：
   - 打開用戶腳本管理器的 **「創建新腳本」** 功能。
   - 將腳本代碼複製並貼到腳本編輯器中。
   - 保存腳本。
3. 打開目標網站，例如 **[fc2ppvdb.com](https://fc2ppvdb.com/)**，確認腳本是否正常執行。

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
| `missav.ws`        | 包含詳細影片信息的高質量站點   |
| `7mmtv.sx`          | 支援多分類影片資源的搜尋站點   |
| `javfc2.xyz`        | 專注於 FC2 影片的搜索引擎      |
| `sukebei.nyaa.si`   | 提供成人內容的 BT 資源搜索引擎 |
| `supjav.com`        | 成人視頻搜索引擎，支持多種分類 |
| `3xplanet.com`      | 集合多種成人資源的搜索網站     |

---

# **開發者指南 (DEVELOPER GUIDE)**

## **簡介**
此文檔專為 **fc2ppvdb_ASVL** 腳本的開發者和貢獻者設計，幫助你理解腳本的架構、主要功能模塊以及如何擴展支持新的站點或自定義功能。

---

## **項目架構**

腳本採用了 **面向對象編程 (OOP)** 的設計，主要分為以下模塊：

1. **Utils 工具類**：
   - 提供常用的輔助工具函數，例如顯示/移除加載提示、創建按鈕、緩存數據等。
   - 文件中的靜態方法可以直接調用，不需要實例化。
2. **Site 類**：
   - 每個支持的影片資源站點會實例化為一個 `Site` 對象。
   - 包含站點的搜索 URL、響應處理邏輯和按鈕生成邏輯。
3. **SearchManager 管理類**：
   - 作為統一的管理中心，負責管理多個站點的搜索任務。
   - 將 FC2PPVDB 的影片編號分配給各個站點進行搜索，並處理結果。
4. **主腳本邏輯**：
   - 創建 `SearchManager` 實例，初始化所有站點，並啟動搜索。

---

## **腳本架構細節**

### **1. Utils 工具類**
工具類包含常用的靜態方法，代碼位於腳本的開頭部分。以下是主要方法的介紹：

- **`showLoading(element, siteName)`**
  - 用於在指定的 HTML 元素旁顯示加載提示。
  - **參數**：
    - `element`：目標 HTML 元素。
    - `siteName`：站點名稱。
  - **返回值**：
    - 返回創建的加載提示元素。
  - **示例**：
    ```javascript
    const loadingElement = Utils.showLoading(targetElement, '123av.com');
    ```

- **`removeLoading(loadingElement)`**
  - 用於移除指定的加載提示。
  - **參數**：
    - `loadingElement`：需要移除的加載提示元素。
  - **示例**：
    ```javascript
    Utils.removeLoading(loadingElement);
    ```

- **`createButton(url, text, bgColorClass)`**
  - 用於創建一個跳轉按鈕。
  - **參數**：
    - `url`：按鈕的目標鏈接。
    - `text`：按鈕的顯示文字。
    - `bgColorClass`：按鈕的背景顏色樣式。
  - **返回值**：
    - 返回生成的按鈕元素。
  - **示例**：
    ```javascript
    const button = Utils.createButton('https://example.com', '跳轉', 'bg-blue-500');
    ```

- **`cacheResult(key, data, expiryHours)`**
  - 用於將搜索結果緩存到瀏覽器中。
  - **參數**：
    - `key`：緩存鍵。
    - `data`：需要緩存的數據。
    - `expiryHours`：緩存過期時間（默認 12 小時）。
  - **示例**：
    ```javascript
    await Utils.cacheResult('123av_abc123', { url: 'https://123av.com' });
    ```

- **`getCachedResult(key)`**
  - 用於獲取緩存的搜索結果。
  - **參數**：
    - `key`：緩存鍵。
  - **返回值**：
    - 返回緩存的數據或 `null`。
  - **示例**：
    ```javascript
    const cachedData = await Utils.getCachedResult('123av_abc123');
    ```

---

### **2. Site 類**
`Site` 類負責處理每個站點的搜索邏輯和響應解析。以下是關鍵屬性和方法：

- **屬性**
  - `name`：站點名稱。
  - `searchUrlFunc`：生成搜索 URL 的函數。
  - `responseHandler`：處理搜索結果響應的函數。
  - `buttonColor`：按鈕的背景顏色。
  - `queue`：搜索任務隊列。
  - `maxConcurrentSearches`：最大並行搜索數量。
  - `queryInterval`：搜索間隔時間。

- **方法**
  - **`addToQueue(id, element)`**
    - 將搜索任務添加到隊列中。
    - **參數**：
      - `id`：影片編號。
      - `element`：目標 HTML 元素。
    - **示例**：
      ```javascript
      site.addToQueue('FC2PPV-123456', targetElement);
      ```

  - **`processQueue()`**
    - 處理搜索隊列，控制並行請求數量和搜索間隔。
    - 自動調用 `search` 方法執行搜索。

  - **`search(id, element)`**
    - 發送搜索請求並處理結果。
    - **參數**：
      - `id`：影片編號。
      - `element`：目標 HTML 元素。

  - **`addButton(element, url)`**
    - 在指定元素旁生成按鈕。
    - **參數**：
      - `element`：目標 HTML 元素。
      - `url`：按鈕跳轉的目標鏈接。

---

### **3. SearchManager 管理類**
`SearchManager` 是腳本的核心管理模塊，負責統一管理多個站點的搜索任務。

- **屬性**
  - `sites`：存儲所有站點的數組。

- **方法**
  - **`addSite(site)`**
    - 添加新的站點實例到 `sites` 中。
    - **參數**：
      - `site`：需要添加的 `Site` 實例。
    - **示例**：
      ```javascript
      manager.addSite(new Site('123av', searchUrlFunc, responseHandler, 'bg-blue-500'));
      ```

  - **`initializeSearch()`**
    - 初始化搜索流程，掃描頁面上的影片編號並分配搜索任務。
    - **示例**：
      ```javascript
      manager.initializeSearch();
      ```

---

## **如何新增站點**

### **步驟 1：定義搜索邏輯**
1. 創建一個新的 `Site` 實例。
2. 實現 `searchUrlFunc` 函數，用於生成搜索 URL。
3. 實現 `responseHandler` 函數，用於處理搜索結果。

### **步驟 2：將站點添加到 SearchManager**
在主腳本中，調用 `manager.addSite()`，並傳入新建的 `Site` 實例。

### **示例**
以下是新增站點的完整示例：
```javascript
manager.addSite(new Site(
    'NewSite',
    id => `https://newsite.com/search?q=${id}`, // 搜索 URL 函數
    (response, id, previewData) => {
        const parser = new DOMParser();
        const doc = parser.parseFromString(response.responseText, "text/html");
        const result = doc.querySelector('a.result'); // 假設搜索結果的鏈接標籤為 <a class="result">
        if (result) {
            previewData.url = result.href; // 提取結果 URL
        }
    },
    'bg-green-500', // 按鈕的背景顏色
    1000, // 搜索間隔（毫秒）
    5 // 最大並行搜索數量
));
