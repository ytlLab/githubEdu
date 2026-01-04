## 從網頁複製repositories到本地資料夾進行操作

在 GitHub 的世界中，**Repository（儲存庫，簡稱 Repo）** 就像是你的專案雲端資料夾。將雲端的專案下載到自己電腦的過程，我們稱為  **Clone（複製/克隆）** 。

使用 **GitHub Desktop** 是最直覺的方式，因為它提供圖形介面，讓你不需要輸入複雜的指令（如 `git clone`）。

### 第一步：在 GitHub 網頁找到專案網址

首先，你需要告訴 GitHub Desktop 你要下載哪一個專案。

1. 開啟瀏覽器，進入你想複製的 GitHub 專案頁面。
2. 點擊綠色的 **「<> Code」** 按鈕。
3. 在彈出的視窗中，確認選分頁位在  **Local** 。
4. 你有兩個選擇：
   * **方法 A：** 點擊  **「Open with GitHub Desktop」** 。這會直接喚起你電腦中的軟體。
   * **方法 B：** 複製下方的  **HTTPS 網址** （例如 `https://github.com/user/repo.git`）。

### 第二步：使用 GitHub Desktop 進行複製

如果你選擇了方法 A，軟體會自動彈出；如果你選擇方法 B，請手動開啟 GitHub Desktop 並執行以下操作：

1. 點擊選單列的 **File** ->  **Clone repository...** 。
2. 在彈出的視窗中，選擇 **URL** 標籤。
3. **Repository URL：** 貼上剛才複製的專案網址。
4. **Local Path：** 這是最重要的步驟。點擊 **Choose...** 選擇你想把這個專案放在電腦裡的哪個位置（例如：`D:\MyProjects`）。
5. 點擊底部的 **Clone** 按鈕。

---

### 第三步：確認完成

等待進度條跑完後，GitHub Desktop 的介面會發生變化：

* **Current Repository：** 左上角會顯示你剛剛複製的專案名稱。
* **本地檔案：** 你可以打開電腦的檔案瀏覽器，進到剛才設定的路徑，就會看到所有的程式碼檔案已經躺在那裡了。

---

### 補充：為什麼要用 Clone 而不是直接 Download ZIP？

雖然 GitHub 網頁提供「Download ZIP」選項，但建議使用 **Clone** 的原因有：

* **版本追蹤：** Clone 會建立連結，讓你未來可以一鍵「Pull（拉取）」雲端的新改動，或「Push（推送）」你的修改。
* **分支管理：** 你可以輕鬆切換不同的開發分支。
* **歷史紀錄：** 你可以看到每一行程式碼是誰在什麼時候修改的。

---

完成  **Clone** （複製）之後，接下來的操作流程通常稱為「開發循環」。你會在 **VS Code** 編輯程式碼，然後透過 **GitHub Desktop** 將改動同步回雲端。

---

### 第一步：從 GitHub Desktop 開啟 VS Code

你可以直接透過 GitHub Desktop 快速開啟編輯器，這樣它會自動鎖定該專案資料夾。

1. 在 GitHub Desktop 中，確認左上角的 **Current Repository** 是你要編輯的專案。
2. 點擊右側面板上的 **「Open in Visual Studio Code」** 按鈕。
   * *如果沒看到按鈕，可以點選上方選單：`Repository` -> `Open in Visual Studio Code` (快捷鍵 `Ctrl + Shift + A`)。*

---

### 第二步：在 VS Code 進行編輯

1. 在 VS Code 左側的檔案瀏覽器中，點開你想修改的檔案。
2. 進行程式碼編寫或修改（例如：新增一個 `index.html` 或修改 `README.md`）。
3. **務必存檔：** 按下 `Ctrl + S` (Windows) 或 `Cmd + S` (Mac) 儲存變更。
   * *你會發現 VS Code 左側的「原始檔控制」圖示出現了藍色或數字標記，這代表它偵測到了變更。*

---

### 第三步：提交變更 (Commit)

回到  **GitHub Desktop** ，你會看到剛才在 VS Code 修改的內容出現在左側清單中。

1. **勾選檔案：** 確認左側你想上傳的檔案已被勾選。
2. **填寫摘要 (Summary)：** 在左下角的小框框輸入這次改動的重點（例如：`Initial commit` 或 `修正登入頁面 Bug`）。
3. **點擊 Commit to main：** 這會將改動記錄在「你電腦裡的」Git 歷史中，但還沒傳到網路上。

---

### 第四步：推送到網頁儲存庫 (Push)

最後一步是將本地的紀錄上傳到 GitHub 伺服器。

1. 點擊頂部橫條的 **「Push origin」** 按鈕。
2. 等待上方進度條跑完。
3. **驗證：** 回到 GitHub 網頁重新整理專案頁面，你就會看到檔案已經更新，且顯示你剛才寫的摘要文字。
