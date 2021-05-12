# Predefined Variables
---
Superglobals
```
https://www.php.net/manual/en/language.variables.superglobals.php
```
---
## $GLOBALS
https://www.php.net/manual/en/reserved.variables.globals.php
```
$ GLOBALS —引用全局範圍內的所有可用變量

描述¶
包含對所有變量的引用 的關聯數組，這些變量當前在腳本的全局範圍內定義。變量名是數組的鍵。
```
## $_SERVER
```
$ _SERVER —服務器和執行環境信息

描述¶
$ _SERVER是一個包含標題，路徑和腳本位置等信息的數組。該數組中的條目由Web服務器創建。不能保證每個Web服務器都可以提供其中的任何一個。服務器可能會省略某些服務器，或提供此處未列出的其他服務器。就是說，»CGI / 1.1規範中說明了很多這些變量，因此您應該可以期待這些變量。

指標¶
您可能會或可能不會在$ _SERVER中找到以下任何元素 。請注意，如果在命令行上運行PHP，那麼將很少（如果有的話）可用（或者實際上有任何意義） 。

' PHP_SELF '
當前正在執行的腳本的文件名，相對於文檔根目錄。例如， 地址為http://example.com/foo/bar.php的腳本中的$ _SERVER ['PHP_SELF'] 將為/foo/bar.php。該__FILE__ 常量包含當前的完整路徑和文件名（例如包含文件）。 如果PHP作為命令行處理器運行，則此變量包含腳本名稱。
' argv '
傳遞給腳本的參數數組。當腳本在命令行上運行時，這將為命令行參數提供C風格的訪問。通過GET方法調用時，它將包含查詢字符串。
' argc '
包含傳遞給腳本的命令行參數的數量（如果在命令行上運行）。
' GATEWAY_INTERFACE '
服務器正在使用什麼版本的CGI規範；例如' CGI/1.1'。
' SERVER_ADDR '
當前腳本正在其下執行的服務器的IP地址。
“ SERVER_NAME ”
正在執行當前腳本的服務器主機的名稱。如果腳本在虛擬主機上運行，則將是為該虛擬主機定義的值。
注意： 在Apache 2下，必須設置UseCanonicalName = On 和ServerName。否則，此值反映客戶端提供的主機名，該主機名可能是欺騙的。在與安全性相關的上下文中依賴此值並不安全。

' SERVER_SOFTWARE '
服務器標識字符串，響應請求時在標頭中給出。
' SERVER_PROTOCOL '
請求頁面的信息協議的名稱和修訂版；例如' HTTP/1.0';
' REQUEST_METHOD '
使用哪種請求方法訪問頁面；例如'，GET'，' HEAD，POST'，'，PUT'。
注意事項：

如果請求方法為，則在發送標頭後終止PHP腳本（這意味著在產生任何輸出而沒有輸出緩沖之後）HEAD。

“ REQUEST_TIME ”
請求開始的時間戳。
' REQUEST_TIME_FLOAT '
請求開始的時間戳，以微秒為單位。
' QUERY_STRING '
用於訪問頁面的查詢字符串（如果有）。
' DOCUMENT_ROOT '
服務器配置文件中定義的當前腳本正在其下執行的文檔根目錄。
' HTTP_ACCEPT '
Accept:當前請求中標頭的 內容（如果有）。
' HTTP_ACCEPT_CHARSET '
Accept-Charset:當前請求中標頭的 內容（如果有）。範例：「iso-8859-1,*,utf-8」。
' HTTP_ACCEPT_ENCODING '
Accept-Encoding:當前請求中標頭的 內容（如果有）。範例：「gzip」。
' HTTP_ACCEPT_LANGUAGE '
Accept-Language:當前請求中標頭的 內容（如果有）。範例：「en」。
' HTTP_CONNECTION '
Connection:當前請求中標頭的 內容（如果有）。範例：「Keep-Alive」。
' HTTP_HOST '
Host:當前請求中標頭的 內容（如果有）。
' HTTP_REFERER '
頁面的地址（如果有的話），該頁面將用戶代理引至當前頁面。這是由用戶代理設置的。並非所有的用戶代理都將設置此功能，有些用戶代理提供了將HTTP_REFERER修改為功能的功能。簡而言之，它不能真正被信任。
' HTTP_USER_AGENT '
User-Agent:當前請求中標頭的 內容（如果有）。這是一個字符串，表示正在訪問頁面的用戶代理。一個典型的例子是：Mozilla / 4.5 [en]（X11; U; Linux 2.2.9 i586）。除其他外，您可以將此值與get_browser（）結合使用，以根據用戶代理的功能來調整頁面的輸出。
' HTTPS '
如果通過HTTPS協議查詢腳本，則設置為非空值。
' REMOTE_ADDR '
用戶正在從中查看當前頁面的IP地址。
' REMOTE_HOST '
用戶正在從中查看當前頁面的主機名。反向dns查找基於用戶的 REMOTE_ADDR。
注意： 必須將Web服務器配置為創建此變量。例如，在Apache中，您需要HostnameLookups On 在httpd.conf內部使其存在。另請參見 gethostbyaddr（）。

' REMOTE_PORT '
用戶計算機上用於與Web服務器通信的端口。
' REMOTE_USER '
經過身份驗證的用戶。
' REDIRECT_REMOTE_USER '
經過身份驗證的用戶（如果請求是內部重定向的）。
' SCRIPT_FILENAME '
當前正在執行的腳本的絕對路徑名。

注意事項：

如果腳本CLI中被執行，作為相對路徑，例如file.php或 ../file.php， $ _SERVER ['SCRIPT_FILENAME']將包含由用戶指定的相對路徑。

' SERVER_ADMIN '
Web服務器配置文件中賦予SERVER_ADMIN（對於Apache）偽指令的值。如果腳本在虛擬主機上運行，則將是為該虛擬主機定義的值。
' SERVER_PORT '
Web服務器用於通信的服務器計算機上的端口。對於默認設置，這將是' 80'; 例如，使用SSL會將其更改為您定義的安全HTTP端口。
注意： 在Apache 2下，必須設置UseCanonicalName = On以及UseCanonicalPhysicalPort = On以獲取物理（真實）端口，否則，該值可能會被欺騙，並且可能會或可能不會返回物理端口值。在與安全性相關的上下文中依賴此值並不安全。

' SERVER_SIGNATURE '
包含服務器版本和虛擬主機名的字符串，添加到服務器生成的頁面（如果啟用）。
' PATH_TRANSLATED '
服務器完成任何虛擬到實際的映射後，當前文件的基於文件系統（而不是文檔根目錄）的路徑。
注意： Apache 2用戶可以AcceptPathInfo = On在httpd.conf內部 使用PATH_INFO進行定義。

“ SCRIPT_NAME ”
包含當前腳本的路徑。這對於需要指向自己的頁面很有用。該__FILE__ 常量包含當前的完整路徑和文件名（例如包含文件）。
' REQUEST_URI '
為了訪問該頁面而給出的URI；例如“ /index.html”。
' PHP_AUTH_DIGEST '
在進行摘要HTTP身份驗證時，此變量設置為客戶端發送的“ Authorization”標頭（然後應使用該標頭進行適當的驗證）。
' PHP_AUTH_USER '
執行HTTP身份驗證時，此變量設置為用戶提供的用戶名。
' PHP_AUTH_PW '
執行HTTP身份驗證時，此變量設置為用戶提供的密碼。
' AUTH_TYPE '
執行HTTP身份驗證時，此變量設置為身份驗證類型。
' PATH_INFO '
包含尾隨實際腳本文件名但在查詢字符串之前（如果可用）的任何客戶端提供的路徑名信息。例如，如果通過URL http://www.example.com/php/path_info.php/some/stuff?foo=bar訪問當前腳本，則$ _SERVER ['PATH_INFO']將包含/some/stuff。
' ORIG_PATH_INFO '
PHP處理之前的 原始版本的“ PATH_INFO ”。
```
## $_GET
```
$ _GET — HTTP GET變量

描述¶
通過URL參數（又稱為查詢字符串）傳遞給當前腳本的變量的關聯數組。請注意，不僅為GET請求填充了數組，而且為所有帶有查詢字符串的請求填充了數組。
```
## $_POST
```
$ _POST — HTTP POST變量

描述¶
在請求中 使用application/x-www-form-urlencoded 或multipart/form-data作為HTTP Content-Type時，通過HTTP POST方法傳遞給當前腳本的變量的關聯數組。
```
## $_FILES
```
$ _FILES — HTTP文件上傳變量

描述¶
通過HTTP POST方法上傳到當前腳本的項目 的關聯數組。POST方法上載 部分概述了此數組的結構 。
```
## $_REQUEST
```
$ _REQUEST — HTTP請求變量

描述¶
關聯數組，默認情況下包含 $ _GET， $ _POST和 $ _COOKIE的內容。
```
## $_SESSION
```
$ _SESSION —會話變量

描述¶
包含可用於當前腳本的會話變量的關聯數組。有關如何使用此功能的更多信息，請參見會話功能文檔。
```
## $_ENV
```
$ _ENV —環境變量

描述¶
通過環境方法傳遞給當前腳本的變量 的關聯數組。

這些變量從運行PHP解析器的環境導入到PHP的全局命名空間中。運行PHP的Shell提供了許多功能，並且不同的系統可能運行的是不同種類的Shell，因此無法確定列表。請參閱您的Shell文檔以獲取已定義環境變量的列表。

其他環境變量包括CGI變量，無論PHP是作為服務器模塊還是CGI處理器運行，CGI變量都放置在該變量中。
```
## $_COOKIE
```
$ _COOKIE — HTTP cookie

描述¶
通過HTTP Cookies傳遞給當前腳本的變量 的關聯數組。
```
## $http_response_header
https://www.php.net/manual/en/reserved.variables.httpresponseheader.php
```
$ http_response_header — HTTP響應頭

描述¶
的$ http_response_header 陣列類似於 get_headers（）函數。使用 HTTP包裝器時， $ http_response_header將使用HTTP響應標頭填充。$ http_response_header將在本地範圍內創建。
```
## $argc
https://blog.johnsonlu.org/phpargv%E8%88%87argc/
```
PHP也提供了$argv的變數，裡面存放了用command line輸入的參數

另外還有提供$argc的變數，可以直接用來判斷參數的數量
```
## $argv
https://blog.johnsonlu.org/phpargv%E8%88%87argc/
```
PHP也提供了$argv的變數，裡面存放了用command line輸入的參數

另外還有提供$argc的變數，可以直接用來判斷參數的數量
```


## Deprecated ==> 不在使用了!!
https://www.php.net/manual/en/reserved.variables.phperrormsg.php
$php_errormsg
```
$ php_errormsg —先前的錯誤消息

警告
自PHP 7.2.0起已棄用此功能 。強烈建議不要使用此功能。

請改用error_get_last（）。

描述¶
$ php_errormsg是一個變量，其中包含PHP生成的最後一條錯誤消息的文本。僅當track_errors配置選項處於打開狀態（默認為關閉）時，此變量才在發生錯誤的範圍內可用。

警告
如果設置了用戶定義的錯誤處理程序（set_error_handler（）），則僅當錯誤處理程序返回時，才設置$ php_errormsgfalse。
```

