## 使用 VS code 圖形介面同步資料

1. 打開 **VS Code**
1. 左下角點擊 **帳號圖示 👤**
1. 點選 **Sign in with GitHub**
1. 瀏覽器會打開 GitHub
1. 登入 GitHub → 點 **Authorize**
1. 回到 VS Code，看到已登入即可

![1767488468957](image/gitHubVersion/1767488468957.png)

## 登入後，用 VS Code 終端機輸入以下資料

* 在 VS Code 上方選單**Terminal → New Terminal**
* 輸入以下指令（請換成你自己的資料）：

```
git config --global user.name "你的GitHub使用者名稱"
git config --global user.email "你的GitHub註冊Email"
```

驗證是否成功：

```
git config --global --list
```

## 左側工具列點擊三叉線圖示

1. **開啟原始碼管理：** 點擊 VS Code 左側工具列的 **「三叉線圖示」** (快捷鍵 `Ctrl + Shift + G`)。
2. **暫存變更：** 在「變更 (Changes)」清單旁點擊 **`+`** 號，將檔案變為「暫存的變更 (Staged Changes)」。
3. **輸入提交訊息：** 在上方的輸入框寫下您做了什麼（例如：`initial commit`），然後點擊 **「提交 (Commit)」** 按鈕。
4. **發佈或同步：**

* 如果是第一次上傳，會出現 **「發佈分段 (Publish Branch)」** 按鈕。
* 如果已經關聯過，點擊下方的 **「同步變更 (Sync Changes)」** 或點擊 `...` 選單中的  **「推送 (Push)」** 。
