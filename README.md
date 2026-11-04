# 基本元件：影片切換練習

作者：謝秉育

依《06_基本元件》第 28 頁實作：上方播放器與切換按鈕、中央橫向動物卡片、底部文字輸入框。

[下載 APK 與完整專案](https://github.com/humans048/BasicUIVideo/releases/latest)

已換入使用者於 2026-11-04 提供的 love.mp4 與 handpan.mp4。
兩支影片完整保留，沒有剪輯或轉檔；離線即可播放。
檔案來源與 SHA256 校驗值請看 VIDEO_SOURCES.md。

## 開啟與執行

Android Studio 選 Open，開啟 BasicUIVideo。Gradle JDK 使用 JDK 21。
Android SDK 需安裝 Android 36（Media3 1.11.1 所需）。最低支援 Android 7.0。
Gradle Sync 後選 app，按 Run。
命令列建置：gradlew.bat :app:assembleDebug。

## 功能

- 預設自動播放 love.mp4；按鈕來回切換 love.mp4 和 handpan.mp4，從頭播放。
- 影片播放結束後循環播放。離開應用程式暫停，回到前景繼續。
- 使用 rememberSaveable 保留所選影片與輸入文字，旋轉畫面仍保留選擇。
- 橫向滑動切換十張動物卡片；點圖片顯示動物名稱 Toast。
- 輸入文字會即時顯示內容。

## 主要程式

app/src/main/java/edu/school/basicuivideo/MainActivity.kt

## 執行畫面

以下為 Android 模擬器實際播放兩支影片的截圖。

<img src="docs/screenshots/love.png" width="280" alt="Love 影片播放與作者謝秉育">
<img src="docs/screenshots/handpan.png" width="280" alt="手碟影片播放與切換按鈕">
