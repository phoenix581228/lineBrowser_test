# LINE 瀏覽器偵測 POC

這是一個概念驗證（POC）專案，用於偵測用戶是否使用 LINE 內建瀏覽器，並提供跳轉到外部瀏覽器的選項。

## 版本說明

### 📱 Version 1 - 手動選擇模式
**網址**: https://phoenix581228.github.io/lineBrowser_test/

- ✅ 自動偵測 LINE 內建瀏覽器（支援 iOS 和 Android）
- ✅ 顯示友善的警告對話框
- ✅ 提供開啟外部瀏覽器或繼續使用的選項
- ✅ 顯示詳細的瀏覽器資訊

### 🚀 Version 2 - 自動跳轉模式（實驗性）
**網址**: https://phoenix581228.github.io/lineBrowser_test/index2.html

- ✅ **iOS LINE 瀏覽器 → 嘗試自動開啟 Safari**
- ✅ **Android LINE 瀏覽器 → 自動開啟 Chrome**
- ✅ 3 秒倒數計時，可手動觸發或取消
- ✅ 詳細的執行日誌，方便除錯
- ✅ 測試按鈕，可手動測試各種跳轉方式
- ⚠️ **注意**：iOS 可能因安全限制無法直接開啟 Safari

### 🎯 Version 3 - 智能引導模式（推薦）
**網址**: https://phoenix581228.github.io/lineBrowser_test/index3.html

- ✅ **清楚的圖文操作指引**
- ✅ **iOS**：引導使用選單複製網址 → 開啟 Safari → 貼上
- ✅ **Android**：引導使用選單 → 在 Chrome 中開啟
- ✅ 提供一鍵複製網址功能
- ✅ 更好的視覺設計和用戶體驗
- ✅ 避免技術限制，100% 可靠
- ✅ 根據實際測試優化流程

#### 為什麼需要 Version 3？

由於 iOS 安全機制限制，從 LINE 內建瀏覽器**無法直接程式化開啟 Safari**：
- `x-web-search://` scheme 可能開啟 Google 或其他搜尋應用
- iOS 限制跨應用程式自動啟動
- 最可靠的方法是引導用戶手動操作

## 線上展示

- **Version 1** (手動選擇): https://phoenix581228.github.io/lineBrowser_test/
- **Version 2** (自動跳轉-實驗): https://phoenix581228.github.io/lineBrowser_test/index2.html
- **Version 3** (智能引導-推薦): https://phoenix581228.github.io/lineBrowser_test/index3.html

## 使用方式

### Version 1 - 手動選擇
1. 在 LINE 聊天中分享 Version 1 URL
2. 點擊連結用 LINE 內建瀏覽器開啟
3. 會自動彈出警告對話框，可選擇：
   - 🌐 開啟外部瀏覽器
   - ✓ 繼續使用 LINE 瀏覽器

### Version 2 - 自動跳轉（實驗性）
1. 在 LINE 聊天中分享 Version 2 URL
2. 點擊連結用 LINE 內建瀏覽器開啟
3. 系統自動偵測平台：
   - 🍎 iOS → 3 秒後嘗試跳轉（可能開啟非 Safari 瀏覽器）
   - 🤖 Android → 3 秒後自動跳轉至 Chrome
4. 倒數期間可以：
   - 立即開啟：跳過倒數直接跳轉
   - 取消跳轉：留在 LINE 瀏覽器

### Version 3 - 智能引導（推薦）
1. 在 LINE 聊天中分享 Version 3 URL
2. 點擊連結用 LINE 內建瀏覽器開啟
3. 系統顯示清楚的操作指引：
   - 🍎 **iOS 用戶**：
     1. 點擊右下角的三個點 (⋮)
     2. 選擇「複製連結」或「複製網址」
     3. 開啟 Safari 瀏覽器
     4. 在網址列貼上並前往
   - 🤖 **Android 用戶**：
     1. 點擊右上角選單 (⋮)
     2. 選擇「在 Chrome 中開啟」
4. 可使用「複製網址」按鈕快速複製

## 技術實作

- 純 HTML + CSS + JavaScript
- 無需任何外部依賴
- 響應式設計，支援手機和桌面裝置

## 授權

MIT License
