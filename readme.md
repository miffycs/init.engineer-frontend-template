# 純靠北工程師 前端模板 README.md

![GitHub contributors](https://img.shields.io/github/contributors/init-engineer/init.engineer-frontend-template.svg)
![GitHub stars](https://img.shields.io/github/stars/init-engineer/init.engineer-frontend-template.svg?style=social)

- [官方網站](https://kaobei.engineer)
- [Facebook 正式機 粉絲團](https://www.facebook.com/init.kobeengineer)
- [Facebook 測試機 粉絲團](https://www.facebook.com/kaobei.engineer)
- [Twitter 粉絲團](https://twitter.com/kaobei_engineer)
- [Plurk 粉絲團](https://www.plurk.com/kaobei_engineer)
---
## 簡介

大家好，這是一份純靠北工程師的前端模板，面向的是單純只做局部頁面開發的前端開發者，如果你單純只想寫頁面，那這個 Repository 將是你最適合的模板範例，模板提供了最基本的前端資源，以及更進一步的 `scss`、`package.json`、`webpack.mix.js` ... 等等。

## 我要如何使用？

1. 使用瀏覽器來打開 `index.html` 即可。

---
## 近期活動

### 版主不會寫程式 之 版主不會寫前端

是的！就如同標題，我覺得我不會寫程式，我也不會寫前端，所以希望大家教我寫程式、寫前端，哭哭 QQ

因為 2019 年快結束了，打算來弄個 2019 年的經典文章回顧、排行榜，可能會有「年度釣魚王」、「年度人氣王」之類的，所以一整個網頁頁面可以切出很多個區塊，有興趣參加的，就認領一個區塊下去實作，這是一個偏向前端的協作活動，不使用框架，單純網頁前端下去刻板。

#### 【遊戲規則】
1. 這個活動的模板頁面位於 `/templates/leaderboard-2019.html` 當中，有 `標頭`、`內容` 兩個主題，你可以兩個都投稿，也可以擇一投稿，但區塊大小是不能變更的，其餘可以自由發揮。
2. 網站內已經有使用了一些有趣的套件，像是 `Animate.css`、`css-doodle`、`CSShake` ... 等等，所以不推薦再引用更多套件。
3. 你可以引用圖片來讓你的作品更美觀，不過需要注意一下圖片的大小，建議總體不超過 `1 MB` 為主。
4. 整個排行榜會有很多區塊，為了分隔這些區塊，背景圖片請不要讓它留空，也就是不要顯示星星 GIF 背景，例如你可以使用 `css-doodle` 來繪製背景。
5. 活動結束後，會將整個頁面部署到正式機，如果可以的話，請您提供一下 GitHub 帳號，讓每個區塊都會顯示作者。

#### 【投稿指南】
1. 直接在本頁發 `issues` 並且附上您完成的程式碼即可。
2. 直接在 [Discord](https://discord.gg/TCghDUT) 群組中的 `#社群活動` 類別當中的 `#【我不會寫前端】` 頻道投稿。

#### 【簡要問答】
- Ｑ：除了用原本 `Bootstrap` 排版，如果要寫額外 CSS 直接寫在下 `template` 下面嗎？還是要寫哪？
> 你提出一個很棒的問題，這邊我順便詳細解釋一下整個專案對於樣式的寫法。
>
> 如果單純只會 CSS 的話，直接在 `<head>` 當中加入 `<style>` 標籤，並在裡面開始撰寫 CSS 即可。
>
> 不過我會推薦學一下 SCSS，將其寫在 `/resources/scss/frontend/pages/_leaderboard.scss` 當中，並且透過 `npm` 或其他你所能學到的前端工具去編譯，相關的檔案例如 `package.json` 或 `webpack.mix.js` 專案都有預先寫好了，所以通常會自動編譯成 `frontend.css` 的壓縮檔案。
>
> 不過我不太建議直接寫 CSS，會建議直接寫 SCSS 就是了。

- Ｑ：請問我要怎麼認領【我不會寫前端】前端切版的模板？
> 你只要下載 `INIT.ENGINEER` 前端模板，去撰寫 `/templates/leaderboard-2019.html` 這份檔案即可，這次的模板總共有分兩種，分別是 `【標題】` 以及 `【年度最佳 xx 文章】`，投稿所需要的資料也都附在註解當中，要注意的是每個模板都要適應 `電腦版` 以及 `手機版`，這個部分已經先幫忙切好了，下面我就把兩個模板都附上來：

```html
<!--
【標題】
  說明：這是排行榜的首頁內容，會簡要的顯示一些數據，其餘的自由發揮。
  必要顯示資料：
    2019 年累積的文章數量 | Example: 2,000
    2019 年累積的社群留言 | Example: 50,000
    2019 年累積的按讚數量 | Example: 300,000
    2019 年累積的分享數量 | Example: 100,000
  非必要，但可自由發揮的資料：
    2019 年累積的刪除文章數量 | Example: 200
    2019 年累積的被封鎖的人數 | Example: 50
-->
<div class="container">
  <!-- 電腦版 -->
  <div class="d-none d-md-flex align-self-md-center justify-content-md-center align-items-md-center vh-100">
    <!-- Something code ... -->
  </div>

  <!-- 手機版 -->
  <div class="d-md-none vh-100 position-relative">
    <!-- Something code ... -->
  </div>
</div>
```

```html
<!--
【年度最佳 xx 文章】
  說明：這個區塊會顯示 2019 年度全部社群平台的讚數加總起來，讚數累計最多的文章。
  必要顯示資料：
    文章的編號                 | Example: #xxxx
    文章的連結                 | Example: https://kaobei.engineer/cards/show/xxxxx
    文章的圖片                 | Example: https://kaobei.engineer/...../image.jpeg
    文章的 Facebook 正式機 讚數 | Example: 2,222
    文章的 Facebook 測試機 讚數 | Example: 1,111
    文章的 Twitter 正式機 讚數  | Example: 555
    文章的 Plurk 正式機 讚數    | Example: 666
    文章的讚數總和              | Example: 4,554
  非必要，但可自由發揮的資料：
    文章的內容                 | Example: 【版主公告】我本來不會寫程式，但自從我參加這場活動之後，我覺得我好像稍微會寫程式了！

  附註說明：圖片的部分，可以用以下圖片做為測試圖片
    - ./public/img/frontend/cards/cards.png
    - ./public/img/frontend/cards/cards-long.png
    - ./public/img/frontend/cards/cards-too-long.png
-->
<div class="container">
  <!-- 電腦版 -->
  <div class="d-none d-md-flex align-self-md-center justify-content-md-center align-items-md-center vh-100">
    <!-- Something code ... -->
  </div>
            
  <!-- 手機版 -->
  <div class="d-md-none vh-100 position-relative">
    <!-- Something code ... -->
  </div>
</div>
```
