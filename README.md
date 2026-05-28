<h1 align="center">🎮 1A2B 數字猜謎大師</h1>

<p align="center">
  <b>一個具備本地 SQLite 排行榜、SharedPreferences 暱稱系統、嚴格防錯驗證與現代感暗黑主題的 Android Java 經典遊戲。</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Version-1.0-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/Platform-Android-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Min_SDK-API_21_(Android_5.0)-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Language-Java-yellow?style=flat-square"/>
  <img src="https://img.shields.io/badge/Database-SQLite-lightgrey?style=flat-square"/>
</p>

---

## 🌟 特色功能 (Features)

本專案非一般的陽春 1A2B 程式，為符合期末專案高規格要求，特別設計並實作了以下功能：

* 👤 **玩家暱稱管理 (Nickname System)** — 透過 `SharedPreferences` 永久記憶您的玩家暱稱，在登入與排行榜中自動套用。
* 📊 **本地 SQLite 資料庫排行榜 (SQLite Database)** — 整合本地 SQLite 資料庫，過關時自動記錄：玩家暱稱、猜題次數、謎底與通關時間，並在排行榜自動排序呈現。
* 🏆 **個人最佳紀錄 (Best Record)** — 首頁會自動搜尋該玩家的歷史通關數據，顯示生涯「最少答題次數」，並在破關超越自我時跳出 `🏆 恭喜！這是一個新的個人最佳紀錄！` 慶祝提示。
* 🛡️ **強大的輸入防呆防錯 (Validation)** — 針對非數字、字數不足（非4位）及重複數字（例如 `1123`）進行即時攔截並顯示 error，避免程式異常崩潰。
* 🌙 **科技風暗黑主題 (Material Design UI)** — 套用 Material Components 打造高質感的 Dark Mode 介面，並以綠、橘雙色 Badge 泡泡動態呈現 `XAXB` 的猜測歷程。
* 🔑 **除錯專用開發人員密技 (Cheat Mode)** — 在遊戲中連點「目前猜測次數」標題 5 下，底部會自動以 Toast 彈出正確答案，方便評分或快速除錯測試。

---

## ⚙️ 系統需求 (Requirements)

* **開發工具**：Android Studio (Giraffe / Hedgehog / Jellyfish / Koala 或更新版本)
* **Gradle 版本**：8.4
* **最小支援版本**：Android 5.0 (API Level 21) 以上
* **開發語言**：Java 8

---

## 🚀 快速開始 (Quick Start)

### 1. 複製專案
```bash
git clone https://github.com/FU-JIYUN/NumberGuessing1A2B.git
```

### 2. 匯入 Android Studio
1. 開啟 Android Studio。
2. 選擇 **File -> Open** 並選取您複製下來的 `NumberGuessing1A2B` 資料夾。
3. 點選 **Sync Now**（Gradle 同步需要 1~2 分鐘）。
4. 點選上方工具列的 **Run** (綠色三角形按鈕) 部署至您的模擬器 (AVD) 或實體 Android 手機中執行。

---

## 🎮 遊戲玩法說明 (How to Play)

系統會隨機產生一個由 4 個不重複數字（0~9）組成的謎題。每次猜測後會得到相對應的提示：
* **A** 代表：數字與位置完全正確的數量。
* **B** 代表：數字正確但位置不對的數量。

> **舉例說明**：
> 如果謎底為 `1234`，而您猜測 `1356`：
> * 數字 `1` 位置正確，計為 **1A**。
> * 數字 `3` 存在但位置不對，計為 **1B**。
> * 因此畫面會提示：`1A1B`。
> * 當猜測結果為 `4A0B` 時，代表成功解開謎題！

---

## 📂 專案目錄結構 (Project Structure)

```text
NumberGuessing1A2B/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/example/guess1a2b/
│   │   │   │   ├── adapter/         # RecyclerView 適配器 (GuessAdapter, LeaderboardAdapter)
│   │   │   │   ├── db/              # SQLite 資料庫輔助類 (DatabaseHelper)
│   │   │   │   ├── model/           # 資料模型 (ScoreRecord, GuessHistory)
│   │   │   │   ├── MainActivity.java
│   │   │   │   ├── GameActivity.java
│   │   │   │   └── LeaderboardActivity.java
│   │   │   ├── res/                 # 資源檔 (Layouts, Themes, Colors, Strings)
│   │   │   └── AndroidManifest.xml
│   │   └── build.gradle
├── gradle/wrapper/                  # Gradle 封裝設定 (Gradle 8.4)
├── build.gradle                     # 專案級 Gradle
├── gradle.properties                # 啟用 AndroidX 支援
└── settings.gradle
```

---

## 👥 作者與學術誠信聲明
* **學號**：U12157131
* **姓名**：（請填寫您的姓名）
* **GitHub 專案網址**：https://github.com/FU-JIYUN/NumberGuessing1A2B
* 本專案為 114 學年度第二學期「Android 行動通訊程式設計」期末報告作業，供個人學術評分使用。
