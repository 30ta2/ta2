# 🎨 刺青工作室 - 新增頁面完整部署指南

## 📋 新增的頁面文件

### 主要頁面（3個）
1. **appointment.html** - 預約服務頁面
2. **contact.html** - 聯絡我們頁面
3. **article1.html** - 刺青前必知的5件事
4. **article2.html** - 刺青風格完整指南
5. **article3.html** - 刺青後的保養秘訣

---

## 🔗 主頁中如何修改連結

### 修改位置1：預約服務區塊

**原始代碼（需要修改）：**
```html
<!-- Appointment Section -->
<section class="appointment" id="appointment">
  <div class="appointment__container">
    <div class="section__header">
      <h2 class="section__title">預約服務</h2>
      <p class="section__subtitle">填寫表單預約您的刺青時間，我們將盡快與您聯繫</p>
    </div>
    <form class="appointment__form" id="appointmentForm">
      <!-- 表單內容 -->
    </form>
  </div>
</section>
```

**改為（新版本）：**
```html
<!-- Appointment Section -->
<section class="appointment" id="appointment">
  <div class="appointment__container">
    <div class="section__header">
      <h2 class="section__title">預約服務</h2>
      <p class="section__subtitle">填寫表單預約您的刺青時間，我們將盡快與您聯繫</p>
    </div>
    <div style="text-align: center;">
      <a href="appointment.html" class="hero__cta">進入預約頁面</a>
    </div>
  </div>
</section>
```

**新增的 HTML：**
```html
<!-- 放在 <article-card> 之前的地方，新增一個連結到預約頁面 -->
<div style="grid-column: 1 / -1; text-align: center; margin-bottom: var(--space-32);">
  <a href="appointment.html" style="display: inline-block; padding: var(--space-16) var(--space-48); background: var(--color-primary); color: white; text-decoration: none; border-radius: var(--radius-lg); font-weight: var(--font-weight-semibold);">📅 打開完整預約系統</a>
</div>
```

---

### 修改位置2：文章分享區塊

**原始代碼：**
```html
<div class="article-card">
  <div class="article-card__image">📖</div>
  <div class="article-card__content">
    <h3 class="article-card__title">刺青前必知的5件事</h3>
    <p class="article-card__excerpt">準備好要刺青了嗎？...</p>
    <a href="#" class="article-card__link">閱讀更多</a>
  </div>
</div>
```

**改為：**
```html
<div class="article-card">
  <div class="article-card__image">📖</div>
  <div class="article-card__content">
    <h3 class="article-card__title">刺青前必知的5件事</h3>
    <p class="article-card__excerpt">準備好要刺青了嗎？這些重要事項請務必了解...</p>
    <a href="article1.html" class="article-card__link">閱讀更多</a>
  </div>
</div>

<div class="article-card">
  <div class="article-card__image">🌟</div>
  <div class="article-card__content">
    <h3 class="article-card__title">刺青風格完整指南</h3>
    <p class="article-card__excerpt">從傳統到現代，探索各種刺青風格...</p>
    <a href="article2.html" class="article-card__link">閱讀更多</a>
  </div>
</div>

<div class="article-card">
  <div class="article-card__image">💧</div>
  <div class="article-card__content">
    <h3 class="article-card__title">刺青後的保養秘訣</h3>
    <p class="article-card__excerpt">正確的保養能讓您的刺青保持最佳狀態...</p>
    <a href="article3.html" class="article-card__link">閱讀更多</a>
  </div>
</div>
```

---

### 修改位置3：聯絡我們區塊

**原始代碼：**
```html
<!-- Contact Section -->
<section class="contact" id="contact">
  <div class="contact__container">
    <div class="section__header">
      <h2 class="section__title">聯絡我們</h2>
      <p class="section__subtitle">歡迎透過以下方式與我們聯繫</p>
    </div>
    <!-- 靜態聯絡資訊 -->
  </div>
</section>
```

**改為：**
```html
<!-- Contact Section -->
<section class="contact" id="contact">
  <div class="contact__container">
    <div class="section__header">
      <h2 class="section__title">聯絡我們</h2>
      <p class="section__subtitle">歡迎透過以下方式與我們聯繫或直接發送訊息</p>
    </div>
    
    <!-- 簡略聯絡資訊 -->
    <div class="contact__info">
      <div class="contact__item">
        <div class="contact__icon">📧</div>
        <div class="contact__label">電子郵件</div>
        <div class="contact__value">contact@example.com</div>
      </div>
      <div class="contact__item">
        <div class="contact__icon">📱</div>
        <div class="contact__label">聯絡電話</div>
        <div class="contact__value">+886 912 345 678</div>
      </div>
      <div class="contact__item">
        <div class="contact__icon">📍</div>
        <div class="contact__label">工作室地址</div>
        <div class="contact__value">台灣台北市</div>
      </div>
    </div>

    <!-- 新增：進入完整聯絡頁面 -->
    <div style="text-align: center; margin-top: var(--space-48);">
      <a href="contact.html" class="hero__cta" style="display: inline-block;">💬 發送完整訊息</a>
    </div>
  </div>
</section>
```

---

## 💾 localStorage 功能說明

### 什麼是 localStorage？
localStorage 是瀏覽器本機存儲，用來在手機或電腦上**永久保存數據**（直到用戶手動刪除）。

### 已實現的 localStorage 功能

#### 1️⃣ **預約服務（appointment.html）**

**保存位置：** 瀏覽器本機  
**鑰匙名稱：** `tattoo_appointments`

**如何查看已保存的預約：**
```javascript
// 在瀏覽器開發者工具中執行：
const appointments = JSON.parse(localStorage.getItem('tattoo_appointments'));
console.log(appointments);
```

**保存的數據格式：**
```json
[
  {
    "name": "王小明",
    "phone": "0912-345-678",
    "email": "user@example.com",
    "date": "2025-11-15",
    "style": "traditional",
    "position": "手臂",
    "description": "想要一個龍的圖案",
    "timestamp": "2025-11-08T19:43:00.000Z"
  }
]
```

**手動刪除所有預約：**
```javascript
// 在開發者工具中執行：
localStorage.removeItem('tattoo_appointments');
```

---

#### 2️⃣ **聯絡我們（contact.html）**

**保存位置：** 瀏覽器本機  
**鑰匙名稱：** `tattoo_contact_messages`

**保存的數據格式：**
```json
[
  {
    "name": "李美麗",
    "email": "li@example.com",
    "phone": "0913-456-789",
    "subject": "詢問客製化設計",
    "message": "想要詢問是否可以客製設計...",
    "timestamp": "2025-11-08T19:43:00.000Z"
  }
]
```

---

## 🔧 如何添加更多 localStorage 功能

### 範例：在文章頁面添加「收藏」功能

**第1步：在 `article1.html` 中找到 `<article>` 標籤**

**第2步：在 `article__header` 後添加收藏按鈕**
```html
<div style="text-align: center; margin-bottom: var(--space-32);">
  <button id="favoriteBtn" onclick="toggleFavorite()" style="
    padding: var(--space-12) var(--space-24);
    background: var(--color-secondary);
    border: 1px solid var(--color-border);
    border-radius: var(--radius-lg);
    cursor: pointer;
    font-size: var(--font-size-base);
    transition: all 0.3s ease;
  ">
    ⭐ 收藏此文章
  </button>
</div>
```

**第3步：在 `<script>` 標籤中添加以下代碼**
```javascript
const FAVORITES_KEY = 'tattoo_favorite_articles';

function toggleFavorite() {
  const btn = document.getElementById('favoriteBtn');
  let favorites = JSON.parse(localStorage.getItem(FAVORITES_KEY)) || [];
  
  const articleId = 'article1';
  const isFavorited = favorites.includes(articleId);
  
  if (isFavorited) {
    favorites = favorites.filter(id => id !== articleId);
    btn.textContent = '⭐ 收藏此文章';
  } else {
    favorites.push(articleId);
    btn.textContent = '✅ 已收藏';
  }
  
  localStorage.setItem(FAVORITES_KEY, JSON.stringify(favorites));
}

// 頁面載入時檢查是否已收藏
window.addEventListener('load', function() {
  const favorites = JSON.parse(localStorage.getItem(FAVORITES_KEY)) || [];
  if (favorites.includes('article1')) {
    document.getElementById('favoriteBtn').textContent = '✅ 已收藏';
  }
});
```

---

## 📁 完整文件結構

```
根目錄/
├── index.html              ✅ 主頁（需修改連結）
├── appointment.html        ✅ 預約頁面（localStorage）
├── contact.html            ✅ 聯絡頁面（localStorage）
├── article1.html           ✅ 文章1
├── article2.html           ✅ 文章2
├── article3.html           ✅ 文章3
│
├── project1.html           （之前的工具頁）
├── project2.html
├── project3.html
├── project4.html
├── project5.html
├── project6.html
│
└── 說明文檔/
    ├── navigation-guide.md
    ├── complete-guide.md
    └── 部署指南.md （此文件）
```

---

## 🚀 快速部署步驟

### 步驟1：下載所有新檔案
- appointment.html
- contact.html
- article1.html
- article2.html
- article3.html

### 步驟2：修改 index.html

#### 在檔案中搜尋並修改以下位置：

**位置A：預約服務區塊（搜尋 "Appointment Section"）**
```
將整個區塊替換為連結版本
```

**位置B：文章分享區塊（搜尋 "Articles Section"）**
```
更新三個 <a> 連結指向 article1.html、article2.html、article3.html
```

**位置C：聯絡區塊（搜尋 "Contact Section"）**
```
在原有內容下方添加進入完整聯絡頁面的按鈕
```

### 步驟3：本機測試
1. 將所有檔案放在同一目錄
2. 打開 `index.html`
3. 測試所有連結
4. 在預約/聯絡頁面提交表單
5. 在瀏覽器開發者工具檢查 localStorage

### 步驟4：驗證 localStorage
```javascript
// 打開 Chrome/Safari 開發者工具，在 Console 執行：
localStorage

// 應該看到：
{
  tattoo_appointments: '[]',
  tattoo_contact_messages: '[]'
}
```

---

## 🎯 localStorage 完整操作指南

### 如何在電腦上查看 localStorage

**Chrome 瀏覽器：**
1. 按 `F12` 打開開發者工具
2. 進入 `Application` 標籤
3. 左側選擇 `Local Storage`
4. 選擇您的網站域名
5. 查看所有保存的數據

**Safari 瀏覽器：**
1. 啟用開發者工具（偏好設定 → 進階 → 顯示開發工具選單）
2. 點選 `Develop` → `Show JavaScript Console`
3. 在 Console 中執行 `localStorage`

**Firefox 瀏覽器：**
1. 按 `F12` 打開開發者工具
2. 進入 `Storage` 標籤
3. 選擇左側的 `Local Storage`
4. 查看已保存的網站

### 如何在手機上查看 localStorage

**iPhone：**
- 使用 Safari，長按 → 檢查元素
- 進入 Console，執行 `localStorage`

**Android：**
- Chrome → 開發者工具 → 遠程調試
- 也可用 Firefox，按 `F12`

### 導出所有 localStorage 數據

```javascript
// 在 Console 執行此代碼，會下載 JSON 檔
const data = {
  appointments: JSON.parse(localStorage.getItem('tattoo_appointments')),
  messages: JSON.parse(localStorage.getItem('tattoo_contact_messages'))
};

const link = document.createElement('a');
link.href = 'data:text/json;charset=utf-8,' + encodeURIComponent(JSON.stringify(data, null, 2));
link.download = 'tattoo_backup.json';
link.click();
```

### 清空所有 localStorage

```javascript
// 在 Console 執行：
localStorage.clear();
```

---

## 🔐 安全性提示

⚠️ **注意：** 
- localStorage 存儲在**本機**，不會自動上傳到伺服器
- 關閉瀏覽器後數據**不會刪除**
- 如需備份，手動導出為 JSON 檔案
- 不建議在 localStorage 存儲敏感信息（如密碼）

---

## 📝 測試清單

- [ ] 所有 HTML 檔案都在根目錄
- [ ] 主頁連結正確指向新頁面
- [ ] 預約頁面表單可正常提交
- [ ] 聯絡頁面表單可正常提交
- [ ] localStorage 能正常保存數據
- [ ] 文章頁面可正常瀏覽
- [ ] 返回按鈕功能正常
- [ ] 響應式設計在手機上正常顯示
- [ ] 明暗主題自動切換正常

---

## 💡 後續可擴展功能

1. **用戶帳戶系統** - 使用 localStorage 保存用戶資訊
2. **預約通知** - 在指定日期前提醒用戶
3. **評分系統** - 使用 localStorage 保存評分記錄
4. **購物車** - 保存客戶選中的設計方案
5. **備份系統** - 定期備份 localStorage 到雲端

---

祝您部署順利！有任何問題請參考各頁面中的代碼註解。🎨