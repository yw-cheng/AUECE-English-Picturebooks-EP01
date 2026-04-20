# 🌻 幼兒英語互動繪本 · 例行性活動系列

五本以幼兒園日常為主題的英語互動繪本，涵蓋 **上學、午餐、洗手、午休、回家** 五個例行性活動。每本書都可以點讀、玩單字遊戲、排句子、唱主題曲，還有家長留言板讓大家一起分享育兒心得。

適合 2–6 歲的孩子與他們的家長。

## 📚 五本書

| 書名 | 中文 | 主題 |
|------|------|------|
| [My First Day at School](./my-first-day-at-school/) | 第一天上學 | 分離焦慮、交朋友 |
| [Yummy Lunch Time](./yummy-lunch-time/) | 午餐時間 | 洗手、感謝、用餐 |
| [Wash Your Hands](./wash-your-hands/) | 洗手時間 | 衛生習慣、Health Hero |
| [Quietly, Nap Time](./quietly-nap-time/) | 午休時間 | 安靜、放鬆 |
| [Time to Go Home](./time-to-go-home/) | 回家時間 | 道別、期待明天 |

## ✨ 每本書都有

- **📖 點讀模式** — 點圖就發音，用可愛的 Microsoft Ana 童音
- **🎯 句子排序** — 把單字塊拖到正確位置，排出完整句子
- **⭕ 單字圈叉** — 井字遊戲邊玩邊學英文單字
- **🎵 主題曲** — 可愛童謠唱出故事主題
- **📝 親子學習單** — 附 PDF 可列印，帶回家一起完成任務
- **💬 家長留言板** — 所有家長可以分享心得、鼓勵彼此（使用 Firebase Firestore）

## 🚀 上線方式（三個免費選項）

### 方式 A：GitHub Pages（長期維護推薦）

1. 把這整個資料夾推上 GitHub 成為一個 repo
2. Settings → Pages → Source 選 `main` branch → `/ (root)` → Save
3. 幾分鐘後就會有網址：`https://你的帳號.github.io/repo名稱/`
4. 分享給其他家長即可

### 方式 B：Netlify Drop（最快）

1. 打開 [https://app.netlify.com/drop](https://app.netlify.com/drop)
2. 把整個 `picture-books` 資料夾拖進頁面
3. 馬上得到一個網址可分享

### 方式 C：離線本地打開

不上線也可以 — 雙擊任何一本書的 `index.html` 就能在瀏覽器打開。缺點是留言板會切到「本機預覽模式」，只存在這台瀏覽器。

## 💬 家長留言板設定

五本書都已經連接同一個 Firebase 專案（`picture-book-board`），所以：

- 上線後家長點留言板就能直接看到大家的留言
- 各本書的留言會分開存（`pb_board_i-love-school`、`pb_board_lunch-time`、`pb_board_wash-your-hands`、`pb_board_quietly-nap-time`、`pb_board_time-to-go-home`），不會混在一起
- 如果要改成自己的 Firebase，找每本書 `index.html` 裡 `BOARD_FIREBASE_CONFIG` 的位置，把四個欄位（apiKey、authDomain、projectId、appId）換成你自己的

詳細的 Firebase 設定步驟請看 `Firebase_設定指南.md`（在 `USR/` 資料夾裡）。

## 🎤 發音生成

繪本裡的英文發音已經預先生成為 MP3（使用 Microsoft Edge 免費神經語音 `en-US-AnaNeural`，小女孩童音）。如果之後有新增句子或單字，可以用 `USR/` 裡的 `生成句子排序發音.command`（雙擊執行）重新生成。

## 📐 資料夾結構

```
picture-books/
├── index.html                        ← 首頁（列出五本書）
├── README.md                         ← 本檔案
├── my-first-day-at-school/
│   ├── index.html                    ← 互動繪本主程式
│   ├── pictures/p01.png ~ p08.png    ← 故事插畫
│   ├── audios/                       ← 句子、主題曲、單字發音 MP3
│   ├── vocab/                        ← 單字圖片（用於單字圈叉遊戲）
│   └── *_Worksheet.pdf               ← 親子學習單（可列印）
├── yummy-lunch-time/        ← 同上結構
├── wash-your-hands/         ← 同上結構
├── quietly-nap-time/        ← 同上結構
└── time-to-go-home/         ← 同上結構
```

## 📄 授權與致謝

- 故事文本、插畫、發音 MP3 — 作者與 Claude 合作製作，開放非商業使用
- 英文童音 — Microsoft Edge Neural TTS（`en-US-AnaNeural`）
- 網頁程式碼 — 純 HTML/CSS/JavaScript，零依賴
- 留言板後端 — [Firebase Firestore](https://firebase.google.com/)（免費方案）

如果喜歡這套繪本，歡迎分享給其他家庭 🌿

---

Made with 💛 by yw & Claude
