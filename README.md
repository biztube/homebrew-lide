# Lide

Lide 是一個放投影片、檔案與影片的白板。在白板上留言，電腦上的 Claude Code 會照留言修改頁面、畫圖表或剪影片。

白板存在使用者自己的電腦，執行時用的是使用者自己的 Claude 訂閱。

## 需要的東西

- 一台 Mac，Apple Silicon 與 Intel 都可以
- Claude 的付費訂閱
- 要剪影片的話另外需要 ffmpeg

## 第一步：安裝 Claude Code 並登入

打開「終端機」，貼上下面這行後按 Enter：

```sh
curl -fsSL https://claude.ai/install.sh | bash
```

裝好之後輸入 `claude` 再按 Enter，照畫面指示用自己的 Claude 帳號登入。登入只需要做一次。

## 第二步：安裝 Lide

有 Homebrew 的話，在終端機執行：

```sh
brew install --cask biztube/lide/lide
```

沒有 Homebrew 的話，到 [Releases](https://github.com/biztube/homebrew-lide/releases/latest) 下載 `Lide.dmg`，打開後把 Lide 拖進「應用程式」資料夾。

裝好後從「應用程式」資料夾打開 Lide。

## 要剪影片時

影片剪輯會用到 ffmpeg，用 Homebrew 安裝：

```sh
brew install ffmpeg
```

Lide 打開時找不到 Claude Code 或 ffmpeg，會跳出提示並列出安裝指令。其餘白板功能照常可用，裝好後重開 Lide 即可。

## 白板存在哪裡

白板與上傳的檔案存在 `~/.lide`。移除 Lide 不會刪掉這個資料夾。
