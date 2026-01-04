## 安裝相關套件

1. markdownlint
2. Markdown All in One
3. Office Viewer

預設編輯環境會變成以下圖示

![1767483203524](./image/aboutVscode/1767483203524.png)

也可不安裝第三個套件

## 修改顏色設定

第三個套件環境下無法使用，需切換回內建的markdown格式才可使用快捷鍵。

自定義 Code Snippets (最強大的自動化)

#### 你可以設定一個關鍵字（例如輸入 `color`），按下 Tab 就自動產生變色語法。

1. 點擊 VS Code 左下角齒輪 ⚙️ ->  **使用者程式碼片段 (User Snippets)** 。
2. 搜尋並選擇  **markdown** 。

```
{
  "Red Text": {
    "prefix": "cr",
    "body": ["<span style=\"color:red\">$1</span>$0"]
  },
  "Blue Text": {
    "prefix": "cb",
    "body": ["<span style=\"color:blue\">$1</span>$0"]
  },
  "Green Text": {
    "prefix": "cg",
    "body": ["<span style=\"color:green\">$1</span>$0"]
  }

}
```

**如何使用：**
在 Markdown 檔案中輸入 `cr、cb、cg` 然後按 `Enter`，它會自動產生 `<span style="color:red">在此輸入文字</span>`，且游標會停在顏色位置讓你修改，再按一次 Tab 就能改文字。

#### 檢查 Markdown 專屬設定

VS Code 有時候會針對特定語言停用自動提示。請確認以下兩點：

* **全域設定** ：在 `Editor > Quick Suggestions` 中，確保  **Other** （其他）被設定為  **`on`** 。
* **JSON 設定檔檢查** ：

1. 按下 **`F1`** 或  **`Ctrl + Shift + P`** 。
2. 在上方出現的輸入框中輸入 `Settings`。
3. 選擇  **「偏好設定: 開啟設定 (使用者)」(Preferences: Open Settings (UI))** 。
4. 在上方搜尋列搜尋「Quick Suggestions」

   ![1767484053069](./image/aboutVscode/1767484053069.png)

#### 專門針對 Markdown 開啟

因為 VS Code 在 Markdown 檔案中預設會關閉自動提示，我們需要強制開啟它：

1. 按下 **`F1`** 或  **`Ctrl + Shift + P`**
2. 在上方出現的輸入框中輸入 `Settings`。
3. 選擇 **「偏好設定: 開啟使用者設定 (JSON)」** (Preferences: Open User Settings (JSON))。
4. 這會打開一個 `settings.json` 檔案。
5. 請檢查檔案中是否有 `[markdown]` 這一段，如果沒有，請在最後的大括號 `{ }` 內貼上這段代碼：

```
"[markdown]": {
    "editor.quickSuggestions": {
        "other": true,
        "comments": true,
        "strings": true
    },
    "editor.snippetSuggestions": "top"
}

```
