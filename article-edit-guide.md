# 📝 Article1.html 文章模板編輯指南

## 完整模板結構說明

### 1️⃣ HTML 結構框架

```html
<!DOCTYPE html>
<html lang="zh-TW">
<head>
  <!-- 所有文章通用 Meta 標籤 -->
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
  
  <!-- 重要：修改這一行為您的文章標題 -->
  <meta name="apple-mobile-web-app-title" content="刺青須知">
  <title>刺青前必知的5件事 - 刺青工作室</title>
  
  <!-- PWA 圖標和配置（保持不變） -->
  <link rel="apple-touch-icon" href="...">
  <link rel="manifest" href="...">
  
  <!-- 完整的設計系統 CSS（不要修改） -->
  <style>...</style>
</head>
<body>
  <!-- 導航固定條（保持不變） -->
  <nav class="nav">...</nav>

  <!-- 主要文章區域 -->
  <article class="article">
    
    <!-- 文章頭部（修改這裡） -->
    <div class="article__header">
      <div class="article__date">📅 2025年11月8日 | 📖 閱讀時間約 5 分鐘</div>
      <h1 class="article__title">刺青前必知的5件事</h1>
      <p class="article__excerpt">準備好要刺青了嗎？在踏入刺青工作室之前，有些重要的事情...</p>
    </div>

    <!-- 文章主要內容（修改這裡） -->
    <div class="article__content">
      <h2>標題（使用 h2）</h2>
      <p>段落文本...</p>
      <ul><li>列表項目</li></ul>
      <div class="highlight">提示框</div>
    </div>

    <!-- 文章導航按鈕（修改連結） -->
    <div class="article__nav">
      <a href="article1.html" class="article__nav-link">
        <div class="article__nav-label">← 上一篇</div>
        <div class="article__nav-title">標題</div>
      </a>
      <a href="article2.html" class="article__nav-link">
        <div class="article__nav-label">下一篇 →</div>
        <div class="article__nav-title">標題</div>
      </a>
    </div>
  </article>
</body>
</html>
```

---

## 2️⃣ 快速編輯檢查清單

### 必須修改的 5 個地方：

| 位置 | 原文 | 修改為 |
|------|------|--------|
| `<meta name="apple-mobile-web-app-title">` | `刺青須知` | 您的文章簡短標題 |
| `<title>` | `刺青前必知的5件事 - 刺青工作室` | 您的文章完整標題 - 刺青工作室 |
| `.article__date` | `2025年11月8日 \| 📖 閱讀時間約 5 分鐘` | 修改日期和閱讀時間 |
| `.article__title` | `刺青前必知的5件事` | 您的文章標題 |
| `.article__excerpt` | `準備好要刺青了嗎？...` | 您的文章簡介（50-100字） |

---

## 3️⃣ 文章內容編寫規則

### ✅ 使用標題層級

```html
<h2>主要章節標題</h2>        <!-- 最多級別，用於主要內容分割 -->
<h3>子章節標題</h3>           <!-- 可選，用於次要分割 -->
```

### ✅ 段落和列表

```html
<!-- 單個段落 -->
<p>您的文本內容...</p>

<!-- 無序列表（用 ul） -->
<ul>
  <li>第一點</li>
  <li>第二點</li>
</ul>

<!-- 有序列表（用 ol） -->
<ol>
  <li>第一步</li>
  <li>第二步</li>
</ol>
```

### ✅ 提示框樣式

```html
<!-- 使用 highlight 類別顯示重要提示 -->
<div class="highlight">
  <strong>💡 提示：</strong>您的提示文本
</div>

<!-- 或用於警告 -->
<div class="highlight">
  <strong>⚠️ 注意：</strong>您的警告文本
</div>
```

### ✅ 字體強調

```html
<strong>重點文字</strong>         <!-- 粗體 -->
<em>強調文字</em>                <!-- 斜體 -->
```

---

## 4️⃣ 文章導航按鈕編輯

修改底部的導航連結指向前後文章：

```html
<div class="article__nav">
  <!-- 上一篇文章 -->
  <a href="article1.html" class="article__nav-link">
    <div class="article__nav-label">← 上一篇</div>
    <div class="article__nav-title">刺青前必知的5件事</div>
  </a>
  
  <!-- 下一篇文章 -->
  <a href="article3.html" class="article__nav-link">
    <div class="article__nav-label">下一篇 →</div>
    <div class="article__nav-title">刺青後的保養秘訣</div>
  </a>
</div>
```

### 文章順序參考

- **article1.html** → 刺青前必知的5件事
- **article2.html** → 刺青風格完整指南  
- **article3.html** → 刺青後的保養秘訣

---

## 5️⃣ CSS 設計系統（勿修改）

所有樣式已經內置，您無需修改 CSS。保持這些類別名稱：

| 類別名 | 用途 |
|--------|------|
| `.article__header` | 文章頭部區域 |
| `.article__title` | 文章大標題 |
| `.article__content` | 主要內容區 |
| `.article__content h2` | 內容標題 |
| `.highlight` | 提示/警告框 |
| `.article__nav` | 底部導航 |

---

## 6️⃣ 實際編輯範例

### 原文：
```html
<div class="article__header">
  <div class="article__date">📅 2025年11月8日 | 📖 閱讀時間約 5 分鐘</div>
  <h1 class="article__title">刺青前必知的5件事</h1>
  <p class="article__excerpt">準備好要刺青了嗎？...</p>
</div>

<div class="article__content">
  <h2>1. 了解您的設計與風格</h2>
  <p>刺青是一項永久的決定，所以在做決定前一定要想清楚。</p>
  <ul>
    <li>在 Pinterest、Instagram 上收集靈感</li>
    <li>與刺青師詳細溝通您的想法</li>
  </ul>
  
  <div class="highlight">
    <strong>💡 提示：</strong>瀏覽刺青師的作品集
  </div>
</div>
```

### 修改後：
```html
<div class="article__header">
  <div class="article__date">📅 2025年11月9日 | 📖 閱讀時間約 8 分鐘</div>
  <h1 class="article__title">刺青初學者必看指南</h1>
  <p class="article__excerpt">新手刺青必知的所有知識，從選擇師傅到術後護理的完整指南...</p>
</div>

<div class="article__content">
  <h2>1. 刺青前的準備工作</h2>
  <p>進行刺青前需要做充分準備，包括心理和身體準備。</p>
  <ul>
    <li>收集您喜歡的刺青風格參考圖</li>
    <li>研究符合您風格的刺青師</li>
    <li>了解基本的刺青知識</li>
  </ul>
  
  <div class="highlight">
    <strong>💡 提示：</strong>至少提前一週與刺青師進行諮詢
  </div>
</div>
```

---

## 7️⃣ 完整修改清單

創建新文章時，按順序檢查：

- [ ] 修改 `<meta name="apple-mobile-web-app-title">`
- [ ] 修改 `<title>` 標籤
- [ ] 修改 `.article__date` 日期
- [ ] 修改 `.article__title` 標題
- [ ] 修改 `.article__excerpt` 摘要
- [ ] 編寫 `.article__content` 內容（使用 h2, p, ul/ol, div.highlight）
- [ ] 修改 `.article__nav` 前後文章連結和標題
- [ ] 檢查所有連結是否正確（article1.html, article2.html, article3.html）

---

## 8️⃣ 文件名規範

保持統一命名方式：
- `article1.html` - 第一篇
- `article2.html` - 第二篇
- `article3.html` - 第三篇
- `article4.html` - 如需添加第四篇文章

---

## 9️⃣ 常見錯誤

❌ **錯誤 1：修改 CSS 樣式類名**
```html
<!-- ❌ 錯誤 -->
<div class="article-header">  <!-- 改了類名會破壞樣式 -->

<!-- ✅ 正確 -->
<div class="article__header">  <!-- 保持原類名 -->
```

❌ **錯誤 2：文章導航連結錯誤**
```html
<!-- ❌ 錯誤 -->
<a href="article4.html">  <!-- 不存在的檔案 -->

<!-- ✅ 正確 -->
<a href="article2.html">  <!-- 確實存在的檔案 -->
```

❌ **錯誤 3：h1 標籤使用超過一次**
```html
<!-- ❌ 錯誤 -->
<h1>標題1</h1>
<h1>標題2</h1>

<!-- ✅ 正確 -->
<h1>主標題</h1>
<h2>副標題</h2>
```

---

## 🔟 快速複製模板

準備新文章時，直接複製 article1.html，然後修改以下部分：

```
步驟 1：複製 article1.html → article4.html
步驟 2：打開文件，找到並修改這5個地方
       ✓ apple-mobile-web-app-title
       ✓ <title>
       ✓ .article__date
       ✓ .article__title
       ✓ .article__excerpt
步驟 3：編寫 .article__content 內容
步驟 4：修改 .article__nav 連結
步驟 5：存檔上傳
```

---

## ✅ 完成檢查清單

新文章完成後檢查：

- [ ] 文章標題在 3 個地方都已修改
- [ ] 日期和閱讀時間已更新
- [ ] 所有內容使用正確的 HTML 標籤（h2, p, ul/ol, strong, div.highlight）
- [ ] 文章導航按鈕連結正確
- [ ] 沒有修改任何 CSS 類名
- [ ] 測試連結確保能正常導航
- [ ] 在手機和桌面上都看起來正常

---

就這樣！您已經掌握了完整的編輯技巧。祝您編寫愉快！✨