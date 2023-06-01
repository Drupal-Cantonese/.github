# i.5　指南的約定
最後 [updated](/node/2827281/discuss) 於2023年2月21日

### [](#s-assumptions-and-prerequisites "Permalink to this headline")假設和先決條件
本指南具有以下假設和先決條件：

- 本指南涵蓋了核心軟體的當前主要版本。
- 本指南被組織為主題；有關詳細資訊，請參見 [Section i.3, 「Organization」](/docs/user_guide/en/preface-organization.html "i.3. Organization")。許多主題包括「*先決條件知識*」部分，其中列出了需要其內容知識的其他主題，以了解您正在閱讀的主題。還假定了指南中未涵蓋的一些背景知識；有關詳細資訊，請參見 [Section i.2, 「Audience and Goal」](/docs/user_guide/en/preface-audience.html "i.2. Audience and Goal")。
- 許多任務主題列表「*站點先決條件*」，這是您在網站上完成的任務，然後才能完成您正在閱讀的主題中的任務。
- 本網站先決條件的細節與在本指南中使用的場景有關，該指南為農貿市場建立網站（有關詳細資訊，請參見 [Section i.6, 「Guiding Scenario」](/docs/user_guide/en/preface-scenario.html "i.6. Guiding Scenario")）。您可以將任務調整到自己的情況下，但是您還需要記住確定網站是否滿足任務的站點先決條件時所做的更改。
- 對於 [Section 3.7, 「Running the Interactive Installer」](/docs/user_guide/en/install-run.html "3.7. Running the Interactive Installer") 之後的所有任務主題，也有一個隱式先決條件：您必須在網站上安裝了最新的內容管理軟體的穩定版本，並可以登錄到具有足夠許可權的使用者帳戶任務（例如安裝網站時創建的使用者帳戶，自動具有完整的許可權）。
- 如果您按順序讀取所有主題，並在執行任務主題中執行所有步驟（登錄），則在閱讀它時，您應該為每個主題提供背景知識和站點先決條件。
- 本指南演示了如何使用管理使用者界面執行任務，並在可能的情況下使用 `Drush` 命令行工具的最新穩定版本（請參閱 [Section 3.2, 「Concept: Additional Tools」](/docs/user_guide/en/install-tools.html " Additional Tools")）。您可以隨意使用其他命令行工具，例如 `Drupal Console`（如果查找等效命令），或者現在僅使用管理界面。

### [](#s-text-conventions "Permalink to this headline")文本約定
本指南的文本中使用以下慣例：

-  URL 「*example.com*」是指您網站的基本 URL。請參閱下面的「導航」部分，以獲取有關如何指示網站內部URL的更多詳細資訊。
- 您應該在網站的使用者界面中看到的文本顯示在「*斜體*」中，例如：單擊「*保存配置*」。這僅適用於來自軟體的使用者界面中的文本，而不是上一個主題中輸入的文本。例如，在有關編輯的主題中，您可能會看到以下說明：單擊「*編輯*」在關於頁面的行（「*編輯*」關於頁面是在上一個主題中創建的）。
- 在「*斜體*」中也顯示了 URL，文件名和新引入的術語。
- 您應在 `shell` 命令行鍵入的文本以等寬字體顯示，例如：


```php
drush cache:rebuild
```
- 在本指南中，單詞「*目錄*」始終用於參考文件目錄（有些人更喜歡調用「*文件夾*」）。

### [](#s-navigation "Permalink to this headline")導航
要在本指南中執行大多數任務主題，您需要在網站的管理界面中導航到一個或多個頁面。您可能會在說明中看到類似的內容（在安裝了基本軟體后，這將更有意義）：

在「*管理*」管理菜單中，導航到「*結構* > *分類法*（*`admin/structure/taxonomy`*）」。

這樣的導航指令假設您已安裝了核心工具欄模組，並且此示例意味著在網站頂部的菜單欄中，您需要單擊「*管理*」以公開菜單選擇，然後單擊「*結構*」，然後「*分類法*」，最後，您將使用 URL 「*[`http://example.com/admin/structure/taxonomy`](http://example.com/admin/structure/taxonomy)*」在頁面上（如果您的站點基礎URL為「*[http://example.com](http://example.com)*」）。

![Admin menu](/files/docs/user_guide/en/images/preface-conventions-top-menu.png)

這是另一個例子：

在「*管理*」管理菜單中，導航到「*配置* > *系統* > *基本站點設置*（*`admin/config/system/site-information`*）」。

在此示例中，單擊「*管理*」和「*配置*」后，您需要找到頁面的「*系統*」部分，然後在此中單擊「*基本站點設置*」。之後，您最終會出現「*[`http://example.com/admin/config/system/site-information`](http://example.com/admin/config/system/site-information)*」。

![System section of the Configuration page](/files/docs/user_guide/en/images/preface-conventions-config-system.png)

另一個注意事項：如果您使用的是標準管理核心七主題，則顯示管理界面中的許多「添加」按鈕，上面有 +符號。例如，在管理/內容上，添加新內容按鈕顯示為「*+添加新內容*」。但是，這是主題依賴性的，並不是按鈕上文本的一部分（例如，屏幕讀取器不一定會讀取它），因此在本指南中，約定是不要在該指南上提及 +符號按鈕。

### [](#s-filling-in-forms "Permalink to this headline")填充表格
本指南中的許多任務主題包括您將填寫 Web 表單的步驟。在大多數情況下，將包含表單的屏幕捕獲圖像，以及您需要輸入每個表單欄位的值的表。例如，您可能會看到像下方的表格，解釋了如果您導航到「*配置* > * 系統 * > *站點資訊*（*`admin/config/config/system/site-information`*）」時將看到的網站資訊表單。

  
  
| 欄位名稱 | 說明 | 示例值 |  
| ---- | ---- | ---- |  
| 站點詳細資訊 > 站點名稱 | 您的網站名稱 | 任何城鎮農貿市場 |  
### 署名
英文原文由 [Jennifer Hodgdon](https://www.drupal.org/u/jhodgdon) 撰寫/編輯。

中文繁體由 [Cantonese translation team](https://github.com/Drupal-Cantonese) 翻譯，校對：空缺，一審：空缺，二審：空缺，責編：空缺

 Next [→ i.6. Guiding Scenario](/docs/user_guide/en/preface-scenario.html) Previous [← i.4. Reporting Problems](/docs/user_guide/en/preface-reporting.html)

