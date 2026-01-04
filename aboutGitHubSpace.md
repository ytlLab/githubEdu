在 GitHub 的規範中，1GB 的限制是指 **「單個 Repository（儲存庫）」** 的大小建議值，而不是帳號內所有儲存庫加起來的總和。

簡單來說，每個儲存庫只要分別控制在建議範圍內即可。

以下是針對 GitHub 空間限制的詳細說明：

### 1. 單個 Repository 的限制

* **建議限制：** GitHub 官方「建議」單個儲存庫維持在  **1GB 以下** 。
* **強烈建議限制：** 最好不要超過  **5GB** 。
* **如果超過會怎樣？** 如果您的單個儲存庫超過 1GB，GitHub 可能會寄發電子郵件提醒您縮減大小；如果達到 5GB 以上，可能會影響到推送（Push）或效能，甚至被系統要求清理。

### 2. 單個檔案的限制（Hard Limit）

* **直接推送限制：** 單個檔案超過 **50 MB** 會收到警告，超過 **100 MB** 則會直接被攔截，無法上傳。
* **解決方案：** 如果必須上傳大檔案，需使用  **Git LFS (Large File Storage)** 。

不小心push超過100mb解決方案：

[https://www.fooish.com/git/large-files.html](https://www.fooish.com/git/large-files.html)
