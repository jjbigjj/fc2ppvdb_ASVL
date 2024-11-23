# fc2ppvdb_ASVL (Auto Search Video Links)

**fc2ppvdb_ASVL** 是一个专为 Chrome 浏览器和 Tampermonkey 插件设计的脚本。它能自动在多个资源站点（如 `_123av.com`、`missav.com`、`7mmtv.sx`、`javfc2.xyz`、`sukebei.nyaa.si` 和 `supjav.com`）上搜索视频资源，并在页面上生成快速跳转按钮。

---

## 功能特点

- **多站点支持**：
  - 自动在以下资源站点中搜索：
    - `_123av.com`
    - `missav.com`
    - `7mmtv.sx`
    - `javfc2.xyz`
    - `sukebei.nyaa.si`
    - `supjav.com`
- **自动化搜索**：
  - 根据 `fc2ppvdb` 页面中的视频编号，自动进行资源搜索。
- **结果快速跳转**：
  - 搜索成功后，生成一个彩色按钮，点击即可快速打开搜索结果。
- **优化性能**：
  - 支持多站点并发搜索（默认并发 3 个站点）。
  - 引入缓存机制，提高效率，避免重复搜索。
- **Chrome 专属**：
  - 专为 Chrome 浏览器和 Tampermonkey 插件设计，确保兼容性和性能。

---

## 安装方法

### 1. 安装 Tampermonkey 插件

**Tampermonkey** 是 Chrome 浏览器的用户脚本管理器。您可以通过以下步骤安装：

1. 打开 Chrome 浏览器。
2. 前往 [Tampermonkey 官方扩展页面](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)。
3. 点击 **添加到 Chrome** 按钮，安装扩展。

### 2. 安装脚本

1. 安装完 Tampermonkey 后，点击浏览器右上角的 Tampermonkey 图标。
2. 选择 **“创建新脚本”**。
3. 将脚本代码复制粘贴到编辑器中。
4. 保存脚本，然后返回 **fc2ppvdb** 网站，确保脚本正常运行。

---

## 使用方法

1. 打开 **[fc2ppvdb.com](https://fc2ppvdb.com/)**。
2. 脚本会自动扫描页面上的视频编号。
3. 对每个视频编号，脚本会在支持的资源站点中搜索资源：
   - 如果找到资源，页面上会生成一个跳转按钮。
   - 点击按钮即可在新标签页中打开对应站点的搜索结果页面。
4. 如果没有结果，则不会生成按钮。

---

## 支持站点

以下是脚本目前支持的资源站点：

| 网站名称          | 描述                     |
|-------------------|--------------------------|
| `_123av.com`      | 提供多种视频资源搜索      |
| `missav.com`      | 包含大量视频详细信息      |
| `7mmtv.sx`        | 视频资源资源站点          |
| `javfc2.xyz`      | 专注于 FC2 视频搜索       |
| `sukebei.nyaa.si` | 种子资源搜索平台          |
| `supjav.com`      | 提供 SupJav 视频搜索支持  |

---

## 默认设置

脚本默认启用了所有站点的搜索功能，并发搜索数量为 3。以下是默认设置：

```javascript
const defaultSettings = {
    enable_123av: true,     // 启用 _123av 搜索
    enableMissAV: true,     // 启用 missav 搜索
    enable7MMTV: true,      // 启用 7mmtv 搜索
    enableJAVFC2: true,     // 启用 javfc2 搜索
    enableSukebei: true,    // 启用 sukebei 搜索
    enableSupJav: true,     // 启用 supjav 搜索
    maxConcurrentSearches: 3, // 默认并发搜索数量
};
