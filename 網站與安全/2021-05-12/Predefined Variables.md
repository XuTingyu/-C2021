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

例子¶
Example＃1 $ GLOBALS示例

<?php
function test() {
    $foo = "local variable";

    echo '$foo in global scope: ' . $GLOBALS["foo"] . "\n";
    echo '$foo in current scope: ' . $foo . "\n";
}

$foo = "Example content";
test();
?>
上面的示例將輸出類似於以下內容的內容：

全局範圍中的$ foo：示例內容
當前作用域中的$ foo：局部變量
注意事項¶
注意事項：

這是一個“超全局變量”，即自動全局變量。這只是意味著它可在整個腳本的所有作用域中使用。不需要做 全局變量。在函數或方法中訪問它。

注意： 可變可用性
與所有其他超全局變量不同， $ GLOBALS本質上一直在PHP中可用。

添加便條 添加便條
用戶貢獻的筆記 4注
向上
下
31therandshow在Gmail的點com ¶9年前
As of PHP 5.4 $GLOBALS is now initialized just-in-time. This means there now is an advantage to not use the $GLOBALS variable as you can avoid the overhead of initializing it. How much of an advantage that is I'm not sure, but I've never liked $GLOBALS much anyways.
向上
下
19mstraczkowski在Gmail的點com ¶7年前
Watch out when you are trying to set $GLOBALS to the local variable.

Even without reference operator "&" your variable seems to be referenced to the $GLOBALS

You can test this behaviour using below code

<?php
/**
* Result:
* POST: B, Variable: C
* GLOBALS: C, Variable: C
*/

// Testing $_POST
$_POST['A'] = 'B';

$nonReferencedPostVar = $_POST;
$nonReferencedPostVar['A'] = 'C';

echo 'POST: '.$_POST['A'].', Variable: '.$nonReferencedPostVar['A']."\n\n";

// Testing Globals
$GLOBALS['A'] = 'B';

$nonReferencedGlobalsVar = $GLOBALS;
$nonReferencedGlobalsVar['A'] = 'C';

echo 'GLOBALS: '.$GLOBALS['A'].', Variable: '.$nonReferencedGlobalsVar['A']."\n\n";
向上
下
8著名的googlemail上的vittorio.zamparella¶4年前
I finally found information about superglobals not being found in $GLOBALS:

https://bugs.php.net/bug.php?id=65223&edit=2
-------------------------------------
[2013-07-09 12:00 UTC] johannes @php.net
[...]super-globals (aka. auto globals) are not added to symbol tables by default for performance reasons unless the parser sees need. i.e.

<?php
$_SERVER;
print_r($GLOBALS);
?>

will list it. You can also control this using auto_gloals_jit in php.ini: http://www.php.net/manual/en/ini.core.php#ini.auto-globals-jit
-------------------------------------

http://www.php.net/manual/en/language.variables.variable.php
-------------------------------------
Warning
Please note that variable variables cannot be used with PHP's Superglobal arrays within functions or class methods. The variable $this is also a special variable that cannot be referenced dynamically.
-------------------------------------
向上
下
-42在Gmail的點com stevenjeffries ¶5年前
I ran into the case where I needed to know if my script was in the global scope or not.

You can use $GLOBALS to figure out which case that is:

<?php // file foo.php

$some_unique_prefix_foo = "ok";
if (isset($GLOBALS["some_unique_prefix_foo"])) {
    echo "Foo is in global scope.\n";
} else {
    echo "Foo is NOT in global scope.\n";
}
unset($some_unique_prefix_foo);

// Inside another file.
function test() {
    include "foo.php";
}
test();

?>

Outputs:

Foo is in global scope.
Foo is NOT in global scope.
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
例子¶
Example＃1 $ _SERVER示例

<?php
echo $_SERVER['SERVER_NAME'];
?>
上面的示例將輸出類似於以下內容的內容：

www.example.com
注意事項¶
注意事項：

這是一個“超全局變量”，即自動全局變量。這只是意味著它可在整個腳本的所有作用域中使用。不需要做 全局變量。在函數或方法中訪問它。

另見¶
過濾器擴展
添加便條 添加便條
用戶貢獻的筆記 44個音符
向上
下
342zeufonlinux在Gmail的點com ¶8年前
Just a PHP file to put on your local server (as I don't have enough memory)

<?php
$indicesServer = array('PHP_SELF',
'argv',
'argc',
'GATEWAY_INTERFACE',
'SERVER_ADDR',
'SERVER_NAME',
'SERVER_SOFTWARE',
'SERVER_PROTOCOL',
'REQUEST_METHOD',
'REQUEST_TIME',
'REQUEST_TIME_FLOAT',
'QUERY_STRING',
'DOCUMENT_ROOT',
'HTTP_ACCEPT',
'HTTP_ACCEPT_CHARSET',
'HTTP_ACCEPT_ENCODING',
'HTTP_ACCEPT_LANGUAGE',
'HTTP_CONNECTION',
'HTTP_HOST',
'HTTP_REFERER',
'HTTP_USER_AGENT',
'HTTPS',
'REMOTE_ADDR',
'REMOTE_HOST',
'REMOTE_PORT',
'REMOTE_USER',
'REDIRECT_REMOTE_USER',
'SCRIPT_FILENAME',
'SERVER_ADMIN',
'SERVER_PORT',
'SERVER_SIGNATURE',
'PATH_TRANSLATED',
'SCRIPT_NAME',
'REQUEST_URI',
'PHP_AUTH_DIGEST',
'PHP_AUTH_USER',
'PHP_AUTH_PW',
'AUTH_TYPE',
'PATH_INFO',
'ORIG_PATH_INFO') ;

echo '<table cellpadding="10">' ;
foreach ($indicesServer as $arg) {
    if (isset($_SERVER[$arg])) {
        echo '<tr><td>'.$arg.'</td><td>' . $_SERVER[$arg] . '</td></tr>' ;
    }
    else {
        echo '<tr><td>'.$arg.'</td><td>-</td></tr>' ;
    }
}
echo '</table>' ;

/*

That will give you the result of each variable like (if the file is server_indices.php at the root and Apache Web directory is in E:\web) :

PHP_SELF    /server_indices.php
argv    -
argc    -
GATEWAY_INTERFACE    CGI/1.1
SERVER_ADDR    127.0.0.1
SERVER_NAME    localhost
SERVER_SOFTWARE    Apache/2.2.22 (Win64) PHP/5.3.13
SERVER_PROTOCOL    HTTP/1.1
REQUEST_METHOD    GET
REQUEST_TIME    1361542579
REQUEST_TIME_FLOAT    -
QUERY_STRING   
DOCUMENT_ROOT    E:/web/
HTTP_ACCEPT    text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
HTTP_ACCEPT_CHARSET    ISO-8859-1,utf-8;q=0.7,*;q=0.3
HTTP_ACCEPT_ENCODING    gzip,deflate,sdch
HTTP_ACCEPT_LANGUAGE    fr-FR,fr;q=0.8,en-US;q=0.6,en;q=0.4
HTTP_CONNECTION    keep-alive
HTTP_HOST    localhost
HTTP_REFERER    http://localhost/
HTTP_USER_AGENT    Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.17 (KHTML, like Gecko) Chrome/24.0.1312.57 Safari/537.17
HTTPS    -
REMOTE_ADDR    127.0.0.1
REMOTE_HOST    -
REMOTE_PORT    65037
REMOTE_USER    -
REDIRECT_REMOTE_USER    -
SCRIPT_FILENAME    E:/web/server_indices.php
SERVER_ADMIN    myemail@personal.us
SERVER_PORT    80
SERVER_SIGNATURE   
PATH_TRANSLATED    -
SCRIPT_NAME    /server_indices.php
REQUEST_URI    /server_indices.php
PHP_AUTH_DIGEST    -
PHP_AUTH_USER    -
PHP_AUTH_PW    -
AUTH_TYPE    -
PATH_INFO    -
ORIG_PATH_INFO    -

*/
?>
向上
下
32tiscali上的vcoletti點它¶1年前
To list all the $_SERVER parameters, simply do:

foreach ($_SERVER as $parm => $value)  echo "$parm = '$value'\n";

No need to list all possible keys of the array.
向上
下
119弗拉基米爾·科納（Vladimir Kornea） ¶12年前
1. All elements of the $_SERVER array whose keys begin with 'HTTP_' come from HTTP request headers and are not to be trusted.

2. All HTTP headers sent to the script are made available through the $_SERVER array, with names prefixed by 'HTTP_'.

3. $_SERVER['PHP_SELF'] is dangerous if misused. If login.php/nearly_arbitrary_string is requested, $_SERVER['PHP_SELF'] will contain not just login.php, but the entire login.php/nearly_arbitrary_string. If you've printed $_SERVER['PHP_SELF'] as the value of the action attribute of your form tag without performing HTML encoding, an attacker can perform XSS attacks by offering users a link to your site such as this:

<a href='http://www.example.com/login.php/"><script type="text/javascript">...</script><span a="'>Example.com</a>

The javascript block would define an event handler function and bind it to the form's submit event. This event handler would load via an <img> tag an external file, with the submitted username and password as parameters.

Use $_SERVER['SCRIPT_NAME'] instead of $_SERVER['PHP_SELF']. HTML encode every string sent to the browser that should not be interpreted as HTML, unless you are absolutely certain that it cannot contain anything that the browser can interpret as HTML.
向上
下
25pierstoval例如在點com ¶4年前
As PHP $_SERVER var is populated with a lot of vars, I think it's important to say that it's also populated with environment vars.

For example, with a PHP script, we can have this:

    MY_ENV_VAR=Hello php -r 'echo $_SERVER["MY_ENV_VAR"];'
   
Will show "Hello".

But, internally, PHP makes sure that "internal" keys in $_SERVER are not overriden, so you wouldn't be able to do something like this:

    REQUEST_TIME=Hello php -r 'var_dump($_SERVER["REQUEST_TIME"]);'
   
Will show something like 1492897785

However, a lot of vars are still vulnerable from environment injection.

I created a gist here ( https://gist.github.com/Pierstoval/f287d3e61252e791a943dd73874ab5ee ) with my PHP configuration on windows with PHP7.0.15 on WSL with bash, the results are that the only "safe" vars are the following:

PHP_SELF
SCRIPT_NAME
SCRIPT_FILENAME
PATH_TRANSLATED
DOCUMENT_ROOT
REQUEST_TIME_FLOAT
REQUEST_TIME
argv
argc

All the rest can be overriden with environment vars, which is not very cool actually because it can break PHP applications sometimes...

(and I only tested on CLI, I had no patience to test with Apache mod_php or Nginx + PHP-FPM, but I can imagine that not a lot of $_SERVER properties are "that" secure...)
向上
下
38麥克勳爵¶11年前
An even *more* improved version...

<?php
phpinfo(32);
?>
向上
下
8克里斯在ocproducts點com ¶4年前
Guide to absolute paths...

Data: __FILE__
Data type: String
Purpose: The absolute pathname of the running PHP file, including the filename.
Caveat: This is not the file called by the PHP processor, it's what is running. So if you are inside an include, it's the include.
Caveat: Symbolic links are pre-resolved, so don't trust comparison of paths to be accurate.
Caveat: Don't assume all operating systems use '/' for the directory separator.
Works on web mode: Yes
Works on CLI mode: Yes

Data: __DIR__
Data type: String
Purpose: The absolute pathname to the running PHP file, excluding the filename
Caveat: This is not the file called by the PHP processor, it's what is running. So if you are inside an include, it's the include.
Caveat: Symbolic links are pre-resolved, so don't trust comparison of paths to be accurate.
Caveat: Don't assume all operating systems use '/' for the directory separator.
Works on web mode: Yes
Works on CLI mode: Yes

Data: $_SERVER['SCRIPT_FILENAME']
Data type: String
Purpose: The absolute pathname of the origin PHP file, including the filename
Caveat: Not set on all PHP environments, may need setting by copying from __FILE__ before other files are included.
Caveat: Symbolic links are not pre-resolved, use PHP's 'realpath' function if you need it resolved.
Caveat: Don't assume all operating systems use '/' for the directory separator.
Caveat: "Filename" makes you think it is just a filename, but it really is the full absolute pathname. Read the identifier as "Script's filesystem (path)name".
Works on web mode: Yes
Works on CLI mode: Yes

Data: $_SERVER['PATH_TRANSLATED']
Data type: String
Purpose: The absolute pathname of the origin PHP file, including the filename
Caveat: It's probably not set, best to just not use it. Just use realpath($_SERVER['SCRIPT_FILENAME']) (and be aware that itself may need to have been emulated).
Caveat: Symbolic links are pre-resolved, so don't trust comparison of paths to be accurate.
Caveat: Don't assume all operating systems use '/' for the directory separator.
Works on web mode: Yes
Works on CLI mode: No

Data: $_SERVER['DOCUMENT_ROOT']
Data type: String
Purpose: Get the absolute path to the web server's document root. No trailing slash.
Caveat: Don't trust this to be set, or set correctly, unless you control the server environment.
Caveat: May or may not have symbolic links pre-resolved, use PHP's 'realpath' function if you need it resolved.
Caveat: Don't assume all operating systems use '/' for the directory separator.
Works on web mode: Yes
Works on CLI mode: No

Note that if something is not set it may be missing from $_SERVER, or it may be blank, so use PHP's 'empty' function for your test.

Note that if you call "php --info" on the command line then naturally some of these settings are going to be blank, as no PHP file is involved.
向上
下
24MarkAgius在markagius點co點英國¶9年前
You have missed 'REDIRECT_STATUS'

Very useful if you point all your error pages to the same file.

File; .htaccess
# .htaccess file.

ErrorDocument 404 /error-msg.php
ErrorDocument 500 /error-msg.php
ErrorDocument 400 /error-msg.php
ErrorDocument 401 /error-msg.php
ErrorDocument 403 /error-msg.php
# End of file.

File; error-msg.php
<?php
  $HttpStatus = $_SERVER["REDIRECT_STATUS"] ;
  if($HttpStatus==200) {print "Document has been processed and sent to you.";}
  if($HttpStatus==400) {print "Bad HTTP request ";}
  if($HttpStatus==401) {print "Unauthorized - Iinvalid password";}
  if($HttpStatus==403) {print "Forbidden";}
  if($HttpStatus==500) {print "Internal Server Error";}
  if($HttpStatus==418) {print "I'm a teapot! - This is a real value, defined in 1998";}

?>
向上
下
14krinklemail在Gmail的點com ¶8年前
If requests to your PHP script send a header "Content-Type" or/ "Content-Length" it will, contrary to regular HTTP headers, not appear in $_SERVER as $_SERVER['HTTP_CONTENT_TYPE']. PHP removes these (per CGI/1.1 specification[1]) from the HTTP_ match group.

They are still accessible, but only if the request was a POST request. When it is, it'll be available as:
$_SERVER['CONTENT_LENGTH']
$_SERVER['CONTENT_TYPE']

[1] https://www.ietf.org/rfc/rfc3875
向上
下
4馬克·西蒙¶1年前
So near, and yet so far …

$_SERVER has nearly everything you need to know about the current web page environment. Something which would have been handy is easy access to the protocol and the actual web root.

For the protocol, you may or may not have $_SERVER['HTTPS'] and it may or may not be empty. For the web root, $_SERVER['DOCUMENT_ROOT'] depends on the server configuration, and doesn’t work for virtual hosts.

For practical purposes, I normally include something like the following in my scripts:

<?php
    //    Web Root
    //    Usage: include("$root/includes/something.inc.php");
        $root = $_SERVER['WEB_ROOT'] = str_replace($_SERVER['SCRIPT_NAME'],'',$_SERVER['SCRIPT_FILENAME']);

    //    Host & Protocol
    //    Usage: $url = "$protocol://$host/images/something.jpg";
        $host = $_SERVER['HTTP_HOST'];
        $protocol=$_SERVER['PROTOCOL'] = isset($_SERVER['HTTPS']) && !empty($_SERVER['HTTPS']) ? 'https' : 'http';
?>
向上
下
14jonbarnett在Gmail的點com ¶12年前
It's worth noting that $_SERVER variables get created for any HTTP request headers, including those you might invent:

If the browser sends an HTTP request header of:
X-Debug-Custom: some string

Then:

<?php
$_SERVER['HTTP_X_DEBUG_CUSTOM']; // "some string"
?>

There are better ways to identify the HTTP request headers sent by the browser, but this is convenient if you know what to expect from, for example, an AJAX script with custom headers.

Works in PHP5 on Apache with mod_php.  Don't know if this is true from other environments.
向上
下
10托南¶12年前
When using the $_SERVER['SERVER_NAME'] variable in an apache virtual host setup with a ServerAlias directive, be sure to check the UseCanonicalName apache directive.  If it is On, this variable will always have the apache ServerName value.  If it is Off, it will have the value given by the headers sent by the browser.

Depending on what you want to do the content of this variable, put in On or Off.
向上
下
5ywarnier在beeznest點組織¶3年前
Note that $_SERVER['REQUEST_URI'] might include the scheme and domain in certain cases.

This happens, for example, when calling the page through a call to stream_context_create() with a HTTP header of 'request_fulluri' set to 1.

For example:

$http = ['request_fulluri' => 1, /* other params here */];
$context = stream_context_create(array( 'http' => $http ));
$fp = fopen($some_url, 'rb', false, $context);

When outputting $_SERVER['REQUEST_URI'] on the server at $some_url, you will get
https://some_url/some_script.php

Remove the request_fulluri => 1 option, and $_SERVER['REQUEST_URI'] gets back to its "normal":
/some_script.php

Apparently, request_fulluri is useful when using some proxy servers.

In this case, there is no proper way to "detect" if this option was set or not, and you should probably use a combination of other $_SERVER[] elements (like REQUEST_SCHEME, SERVER_NAME and SERVER_PORT) to determine if this was the case.

One quick (and improvable) way to detect it would be to compare the start of the REQUEST_URI with REQUEST_SCHEME:

$scheme = $_SERVER['REQUEST_SCHEME'] . '://';
if (strcmp(substr($_SERVER['REQUEST_URI'], 0, strlen($scheme)), $scheme) === 0) {
    // request_fulluri was set
}
向上
下
16史蒂夫在sc-fa dot com¶11年前
If you are serving from behind a proxy server, you will almost certainly save time by looking at what these $_SERVER variables do on your machine behind the proxy.  

$_SERVER['HTTP_X_FORWARDED_FOR'] in place of $_SERVER['REMOTE_ADDR']

$_SERVER['HTTP_X_FORWARDED_HOST'] and
$_SERVER['HTTP_X_FORWARDED_SERVER'] in place of (at least in our case,) $_SERVER['SERVER_NAME']
向上
下
6Stefano（sarchittu dot org的信息） ¶10年前
A way to get the absolute path of your page, independent from the site position (so works both on local machine and on server without setting anything) and from the server OS (works both on Unix systems and Windows systems).

The only parameter it requires is the folder in which you place this script
So, for istance, I'll place this into my SCRIPT folder, and I'll write SCRIPT word length in $conflen

<?php
$conflen=strlen('SCRIPT');
$B=substr(__FILE__,0,strrpos(__FILE__,'/'));
$A=substr($_SERVER['DOCUMENT_ROOT'], strrpos($_SERVER['DOCUMENT_ROOT'], $_SERVER['PHP_SELF']));
$C=substr($B,strlen($A));
$posconf=strlen($C)-$conflen-1;
$D=substr($C,1,$posconf);
$host='http://'.$_SERVER['SERVER_NAME'].'/'.$D;
?>

$host will finally contain the absolute path.
向上
下
9理查德·約克（Richard York） ¶11年前
Not documented here is the fact that $_SERVER is populated with some pretty useful information when accessing PHP via the shell.

["_SERVER"]=>
  array(24) {
    ["MANPATH"]=>
    string(48) "/usr/share/man:/usr/local/share/man:/usr/X11/man"
    ["TERM"]=>
    string(11) "xterm-color"
    ["SHELL"]=>
    string(9) "/bin/bash"
    ["SSH_CLIENT"]=>
    string(20) "127.0.0.1 41242 22"
    ["OLDPWD"]=>
    string(60) "/Library/WebServer/Domains/www.example.com/private"
    ["SSH_TTY"]=>
    string(12) "/dev/ttys000"
    ["USER"]=>
    string(5) "username"
    ["MAIL"]=>
    string(15) "/var/mail/username"
    ["PATH"]=>
    string(57) "/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin:/usr/X11/bin"
    ["PWD"]=>
    string(56) "/Library/WebServer/Domains/www.example.com/www"
    ["SHLVL"]=>
    string(1) "1"
    ["HOME"]=>
    string(12) "/Users/username"
    ["LOGNAME"]=>
    string(5) "username"
    ["SSH_CONNECTION"]=>
    string(31) "127.0.0.1 41242 10.0.0.1 22"
    ["_"]=>
    string(12) "/usr/bin/php"
    ["__CF_USER_TEXT_ENCODING"]=>
    string(9) "0x1F5:0:0"
    ["PHP_SELF"]=>
    string(10) "Shell.php"
    ["SCRIPT_NAME"]=>
    string(10) "Shell.php"
    ["SCRIPT_FILENAME"]=>
    string(10) "Shell.php"
    ["PATH_TRANSLATED"]=>
    string(10) "Shell.php"
    ["DOCUMENT_ROOT"]=>
    string(0) ""
    ["REQUEST_TIME"]=>
    int(1247162183)
    ["argv"]=>
    array(1) {
      [0]=>
      string(10) "Shell.php"
    }
    ["argc"]=>
    int(1)
  }
向上
下
3克里斯在ocproducts點com ¶4年前
Guide to URL paths...

Data: $_SERVER['PHP_SELF']
Data type: String
Purpose: The URL path name of the current PHP file, including path-info (see $_SERVER['PATH_INFO']) and excluding URL query string. Includes leading slash.
Caveat: This is after URL rewrites (i.e. it's as seen by PHP, not necessarily the original call URL).
Works on web mode: Yes
Works on CLI mode: Tenuous (emulated to contain just the exact call path of the CLI script, with whatever exotic relative pathname you may call with, not made absolute and not normalised or pre-resolved)

Data: $_SERVER['SCRIPT_NAME']
Data type: String
Purpose: The URL path name of the current PHP file, excluding path-info and excluding URL query string. Includes leading slash.
Caveat: This is after URL rewrites (i.e. it's as seen by PHP, not necessarily the original call URL).
Caveat: Not set on all PHP environments, may need setting via preg_replace('#\.php/.*#', '.php', $_SERVER['PHP_SELF']).
Works on web mode: Yes
Works on CLI mode: Tenuous (emulated to contain just the exact call path of the CLI script, with whatever exotic relative pathname you may call with, not made absolute and not normalised or pre-resolved)

Data: $_SERVER['REDIRECT_URL']
Data type: String
Purpose: The URL path name of the current PHP file, path-info is N/A and excluding URL query string. Includes leading slash.
Caveat: This is before URL rewrites (i.e. it's as per the original call URL).
Caveat: Not set on all PHP environments, and definitely only ones with URL rewrites.
Works on web mode: Yes
Works on CLI mode: No

Data: $_SERVER['REQUEST_URI']
Data type: String
Purpose: The URL path name of the current PHP file, including path-info and including URL query string. Includes leading slash.
Caveat: This is before URL rewrites (i.e. it's as per the original call URL). *
*: I've seen at least one situation where this is not true (there was another $_SERVER variable to use instead supplied by the URL rewriter), but the author of the URL rewriter later fixed it so probably fair to dismiss this particular note.
Caveat: Not set on all PHP environments, may need setting via $_SERVER['REDIRECT_URL'] . '?' . http_build_query($_GET) [if $_SERVER['REDIRECT_URL'] is set, and imperfect as we don't know what GET parameters were originally passed vs which were injected in the URL rewrite] --otherwise-- $_SERVER['PHP_SELF'] . '?' . http_build_query($_GET).
Works on web mode: Yes
Works on CLI mode: No

Data: $_SERVER['PATH_INFO']
Data type: String
Purpose: Find the path-info, which is data after the .php filename in the URL call. It's a strange concept.
Caveat: Some environments may not support it, it is best avoided unless you have complete server control
Works on web mode: Yes
Works on CLI mode: No

Note that if something is not set it may be missing from $_SERVER, or it may be blank, so use PHP's 'empty' function for your test.
向上
下
7rulerof在Gmail的點com ¶10年前
I needed to get the full base directory of my script local to my webserver, IIS 7 on Windows 2008.

I ended up using this:

<?php
function GetBasePath() {
    return substr($_SERVER['SCRIPT_FILENAME'], 0, strlen($_SERVER['SCRIPT_FILENAME']) - strlen(strrchr($_SERVER['SCRIPT_FILENAME'], "\\")));
}
?>

And it returned C:\inetpub\wwwroot\<applicationfolder> as I had hoped.
向上
下
7克里斯¶11年前
A table of everything in the $_SERVER array can be found near the bottom of the output of phpinfo();
向上
下
5湯姆¶8年前
Be warned that most contents of the Server-Array (even $_SERVER['SERVER_NAME']) are provided by the client and can be manipulated. They can also be used for injections and thus MUST be checked and treated like any other user input.
向上
下
1個克里斯在ocproducts點com ¶4年前
Guide to script parameters...

Data: $_GET
Data type: Array (map)
Purpose: Contains all GET parameters (i.e. a parsed URL query string).
Caveat: GET parameter names have to be compliant with PHP variable naming, e.g. dots are not allowed and get substituted.
Works on web mode: Yes
Works on CLI mode: No

Data: $_SERVER['QUERY_STRING']
Data type: String
Purpose: Gets an unparsed URL query string.
Caveat: Not set on all PHP environments, may need setting via http_build_query($_GET).
Works on web mode: Yes
Works on CLI mode: No

Data: $_SERVER['argv']
Data type: Array (list)
Purpose: Get CLI call parameters.
Works on web mode: Tenuous (just contains a single parameter, the query string)
Works on CLI mode: Yes
向上
下
3mtprod dot com上的信息¶12年前
On Windows IIS 7 you must use $_SERVER['LOCAL_ADDR'] rather than $_SERVER['SERVER_ADDR'] to get the server's IP address.
向上
下
3PHP在Isoop Dot Net上¶11年前
Use the apache SetEnv directive to set arbitrary $_SERVER variables in your vhost or apache config.

SetEnv varname "variable value"
向上
下
5米爾科·施泰納點在slashdevslashnull點德¶11年前
<?php

// RFC 2616 compatible Accept Language Parser
// http://www.ietf.org/rfc/rfc2616.txt, 14.4 Accept-Language, Page 104
// Hypertext Transfer Protocol -- HTTP/1.1

foreach (explode(',', $_SERVER['HTTP_ACCEPT_LANGUAGE']) as $lang) {
    $pattern = '/^(?P<primarytag>[a-zA-Z]{2,8})'.
    '(?:-(?P<subtag>[a-zA-Z]{2,8}))?(?:(?:;q=)'.
    '(?P<quantifier>\d\.\d))?$/';

    $splits = array();

    printf("Lang:,,%s''\n", $lang);
    if (preg_match($pattern, $lang, $splits)) {
        print_r($splits);
    } else {
        echo "\nno match\n";
    }
}

?>

example output:

Google Chrome 3.0.195.27 Windows xp

Lang:,,de-DE''
Array
(
    [0] => de-DE
    [primarytag] => de
    [1] => de
    [subtag] => DE
    [2] => DE
)
Lang:,,de;q=0.8''
Array
(
    [0] => de;q=0.8
    [primarytag] => de
    [1] => de
    [subtag] =>
    [2] =>
    [quantifier] => 0.8
    [3] => 0.8
)
Lang:,,en-US;q=0.6''
Array
(
    [0] => en-US;q=0.6
    [primarytag] => en
    [1] => en
    [subtag] => US
    [2] => US
    [quantifier] => 0.6
    [3] => 0.6
)
Lang:,,en;q=0.4''
Array
(
    [0] => en;q=0.4
    [primarytag] => en
    [1] => en
    [subtag] =>
    [2] =>
    [quantifier] => 0.4
    [3] => 0.4
)
向上
下
-1webforever dot es上的信息¶3個月前
<?php
//Print all values on screen.
foreach($_SERVER as $x => $v) echo "$x : $v <br>";
?>
向上
下
3wbeaumo1在Gmail的點com ¶10年前
Don't forget $_SERVER['HTTP_COOKIE']. It contains the raw value of the 'Cookie' header sent by the user agent.
向上
下
1個plugwash在p10link點網¶6年前
Be aware that it's a bad idea to access x-forwarded-for and similar headers through this array. The header names are mangled when populating the array and this mangling can introduce spoofing vulnerabilities.

See http://en.wikipedia.org/wiki/User:Brion_VIBBER/Cool_Cat_incident_report for details of a real world exploit of this.
向上
下
3pudding06在Gmail的點com ¶12年前
Here's a simple, quick but effective way to block unwanted external visitors to your local server:

<?php
// only local requests
if ($_SERVER['REMOTE_ADDR'] !== '127.0.0.1') die(header("Location: /"));
?>

This will direct all external traffic to your home page. Of course you could send a 404 or other custom error. Best practice is not to stay on the page with a custom error message as you acknowledge that the page does exist. That's why I redirect unwanted calls to (for example) phpmyadmin.
向上
下
-2丹尼爾·塔哈（Daniel Tahar） ¶11個月前
To expand a bit on the price you could pay for relying on 'HTTP_REFERER': several large news sites I read often have paywalls, with cookies in place so you can only read X articles before you must subscribe; if using Incognito, they count the number of times you accessed via the same IP; everything to get you to subscribe. However, in order to be appealing, any visit where the 'HTTP_REFERER' is Google News will give you the entire article. I'm sure it's a dilemma their webmasters have, but for now any time someone sends you a story on one of them, all you have to do is search for the title and click the result from Google News. Bottom line: never count on it.

PS (1): ofcourse i'm talking about a friend. I pay for content.
PS (2): after some debate, the RFC decided to keep 'HTTP_REFERER', although it's misspelled.
向上
下
1個wyattstorch42在後市點com ¶7年前
<?php
/*
* I wrote this because I was including a file with classes in it. Let's say that
* I have a contact page at mysite.com/contact/index.php and a Form class at
* mysite.com/classes/Form.php. So in index.php, I have this statement:
* require '../classes/Form.php';
* The Form class includes a method to generate the HTML markup for a number of
* form elements, including a CAPTCHA image and associated text field. To do so,
* it must generate an <img /> element and give it a src of Form.php?captcha.
* But I wanted it to automatically generate a src attribute without index.php
* giving it a relative path. This script comes in handy by automatically
* locating the directory that contains the included file (Form.php) and converting
* it from an absolute path to a relative path that could be used for an img src,
* an a href, a link href, etc.
*/
function relativeURL () {
    $dir = str_replace('\\', '/', __DIR__);
        // Resolves inconsistency with PATH_SEPARATOR on Windows vs. Linux
        // Use dirname(__FILE__) in place of __DIR__ for older PHP versions
    return substr($dir, strlen($_SERVER['DOCUMENT_ROOT']));
        // Clip off the part of the path outside of the document root
}

/*
*contact/index.php
*/
require '../classes/Form.php';
new Form()->drawCaptchaField();
    // Writes: <img src="/classes/Form.php?captcha" />

   
/*
* classes/Form.php
*/
if (isset($_GET['captcha'])) {
    // generate/return CAPTCHA image
}

class Form {
    // ...
    public function drawCaptchaField () {
        echo '<img src="'.relativeURL().'?captcha" />';
    }
}
?>
向上
下
1個dtomasiewicz在Gmail的點com ¶10年前
To get an associative array of HTTP request headers formatted similarly to get_headers(), this will do the trick:

<?php
/**
* Transforms $_SERVER HTTP headers into a nice associative array. For example:
*   array(
*       'Referer' => 'example.com',
*       'X-Requested-With' => 'XMLHttpRequest'
*   )
*/
function get_request_headers() {
    $headers = array();
    foreach($_SERVER as $key => $value) {
        if(strpos($key, 'HTTP_') === 0) {
            $headers[str_replace(' ', '-', ucwords(str_replace('_', ' ', strtolower(substr($key, 5)))))] = $value;
        }
    }
    return $headers;
}
?>
向上
下
1個賈羅德在squarecrow點com ¶11年前
$_SERVER['DOCUMENT_ROOT'] is incredibly useful especially when working in your development environment. If you're working on large projects you'll likely be including a large number of files into your pages. For example:

<?php
//Defines constants to use for "include" URLS - helps keep our paths clean

        define("REGISTRY_CLASSES",  $_SERVER['DOCUMENT_ROOT']."/SOAP/classes/");
        define("REGISTRY_CONTROLS", $_SERVER['DOCUMENT_ROOT']."/SOAP/controls/");

        define("STRING_BUILDER",     REGISTRY_CLASSES. "stringbuilder.php");
        define("SESSION_MANAGER",     REGISTRY_CLASSES. "sessionmanager.php");
        define("STANDARD_CONTROLS",    REGISTRY_CONTROLS."standardcontrols.php");
?>

In development environments, you're rarely working with your root folder, especially if you're running PHP locally on your box and using DOCUMENT_ROOT is a great way to maintain URL conformity. This will save you hours of work preparing your application for deployment from your box to a production server (not to mention save you the headache of include path failures).
向上
下
0Pomat在現場點它¶7年前
$_SERVER['DOCUMENT_ROOT'] may contain backslashes on windows systems, and of course it may or may not have a trailing slash (backslash).
I saw the following as an example of the proper way we're supposed to deal with this issue:

<?php
include(dirname($_SERVER['DOCUMENT_ROOT']) . DIRECTORY_SEPARATOR . 'file.php');
?>

Ok, the latter may be used to access a file inside the parent directory of the document root, but actually does not properly address the issue.
In the end, don't warry about. It should be safe to use forward slashes and append a trailing slash in all cases.
Let's say we have this:

<?php
$path = 'subdir/file.php';
$result = $_SERVER['DOCUMENT_ROOT'] . '/' . $path;
?>

On linux $result might be something like
1) "/var/www/subdir/file.php"
2) "/var/www//subdir/file.php"
String 2 is parsed the same as string 1 (have a try with command 'cd').

On windows $result might be something like
1) "C:/apache/htdocs/subdir/file.php"
2) "C:/apache/htdocs//subdir/file.php"
3) "C:\apache\htdocs/subdir/file.php"
4) "C:\apache\htdocs\/subdir/file.php"
All those strings are parsed as "C:\apache\htdocs\subdir\file.php" (have a try with 'cd').
向上
下
1個silverquick在Gmail的點com ¶12年前
I think the HTTPS element will only be present under Apache 2.x. It's not in the list of "special" variables here:
http://httpd.apache.org/docs/1.3/mod/mod_rewrite.html#RewriteCond
But it is here:
http://httpd.apache.org/docs/2.0/mod/mod_rewrite.html#rewritecond
向上
下
1個在nerdgirl點dk上噴射¶12年前
Windows running IIS v6 does not include $_SERVER['SERVER_ADDR']

If you need to get the IP addresse, use this instead:

<?php
$ipAddress = gethostbyname($_SERVER['SERVER_NAME']);
?>
向上
下
0picov在e-link上點它¶9年前
A simple function to detect if the current page address was rewritten by mod_rewrite:

<?php
public function urlWasRewritten() {
  $realScriptName=$_SERVER['SCRIPT_NAME'];
  $virtualScriptName=reset(explode("?", $_SERVER['REQUEST_URI']));
  return !($realScriptName==$virtualScriptName);
}
?>
向上
下
0cupy在電子郵件點CZ ¶11年前
Tech note:
$_SERVER['argc'] and $_SERVER['argv'][] has some funny behaviour,
used from linux (bash) commandline, when called like
"php ./script_name.php 0x020B"
there is everything correct, but
"./script_name.php 0x020B"
is not correct - "0" is passed instead of "0x020B" as $_SERVER['argv'][1] - see the script below.
Looks like the parameter is not passed well from bash to PHP.
(but, inspected on the level of bash, 0x020B is understood well as $1)

try this example:

------------->8------------------
cat ./script_name.php
#! /usr/bin/php

if( $_SERVER['argc'] == 2)
  {
    // funny... we have to do this trick to pass e.g. 0x020B from parameters
    // ignore this: "PHP Notice:  Undefined offset:  2 in ..."
    $EID = $_SERVER['argv'][1] + $_SERVER['argv'][2] + $_SERVER['argv'][3];
  }
else
   {        // default
     $EID = 0x0210; // PPS failure
   }
向上
下
-1斯凱勒¶2年前
A snippet to list the header values:

<?php

echo <<<END
<!DOCTYPE html>
<meta charset="UTF-8" />
<title>\$_SERVER</title>
<style>
    table {
        border-collapse: collapse;
    }
    td {
        border: 1px solid #999;
        padding: 3px;
    }
</style>
<table>
END;

foreach ($_SERVER as $k => $v) {
    $key = htmlentities($k);
    $value = htmlentities($v);
    echo "\n\t<tr>\n\t\t<td>$key\n\t\t<td>$value\n";
}
echo "</table>";
?>
向上
下
-1lemonostif在Gmail的點com ¶1年前
PHP_SELF is a disgrace of a programmer's work. One of the most widespread PHP vulnerabilities since version 4 and the manual says nothing about the dangers. At least clarify that ITS VALUE CAN BE PROVIDED BY THE USER with capitals preferably if you want to make the internet a safer place...
向上
下
-2razvan_bc在雅虎點com ¶2年前
In 2018 things can be pretty cool !!!
look around:

<?php
//save it index.php in a root folder

/*
    if($_SERVER["REQUEST_METHOD"]!='GET'){
        echo('it`s a POST');
    }else{   
        echo('it`s a GET');
    }
*/

$_REQ =& $_SERVER["REQUEST_METHOD"];
($_REQ=='POST')and($what='it`s a POST');
($_REQ=='GET')and($what='it`s a GET');
isset($what) and print($what);

?>
<form method="POST" action="">
<input type="text" name="postbaby" value="sadasdsa">
<input type="submit" value="POST THAT">
</form>
<br>
<form method="GET" action="">
<input type="text" name="getbaby" value="sadasdsa">
<input type="submit" value="GET THAT">
</form>
<hr><?php
phpinfo();
?>

what if you have a class with controllers?
i hope will not be depreciated cause STATIC CALLS I TEST ALREADY ARE VERY FAST:

<?php
//save it index.php in a root folder

/*
    if($_SERVER["REQUEST_METHOD"]!='GET'){
        echo('it`s a POST');
    }else{   
        echo('it`s a GET');
    }
*/
class forms {
    public static function type(){
        return $_SERVER["REQUEST_METHOD"];
    }
    public static function post($f){
        (self::type()=='POST')and $f();
    }
   
    public static function get($f){
        (self::type()=='GET')and $f();
    }
}

?>
<form method="POST" action="">
<input type="text" name="postbaby" value="sadasdsa">
<input type="submit" value="POST THAT">
</form>
<br>
<form method="GET" action="">
<input type="text" name="getbaby" value="sadasdsa">
<input type="submit" value="GET THAT">
</form>
<hr><?php
forms::post(function(){
    $what='it`s a POST';echo($what);
});

forms::get(function(){
    $what='it`s a GET';echo($what);
});
//phpinfo();
?>
向上
下
-32962051004 QQ在點com ¶3年前
<?php
/*
Sometimes you will find that your website will not get the correct user IP after adding CDN, then this function will help you
*/
function real_ip()
{
   $ip = $_SERVER['REMOTE_ADDR'];
    if (isset($_SERVER['HTTP_X_FORWARDED_FOR']) && preg_match_all('#\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}#s', $_SERVER['HTTP_X_FORWARDED_FOR'], $matches)) {
        foreach ($matches[0] AS $xip) {
            if (!preg_match('#^(10|172\.16|192\.168)\.#', $xip)) {
                $ip = $xip;
                break;
            }
        }
    } elseif (isset($_SERVER['HTTP_CLIENT_IP']) && preg_match('/^([0-9]{1,3}\.){3}[0-9]{1,3}$/', $_SERVER['HTTP_CLIENT_IP'])) {
        $ip = $_SERVER['HTTP_CLIENT_IP'];
    } elseif (isset($_SERVER['HTTP_CF_CONNECTING_IP']) && preg_match('/^([0-9]{1,3}\.){3}[0-9]{1,3}$/', $_SERVER['HTTP_CF_CONNECTING_IP'])) {
        $ip = $_SERVER['HTTP_CF_CONNECTING_IP'];
    } elseif (isset($_SERVER['HTTP_X_REAL_IP']) && preg_match('/^([0-9]{1,3}\.){3}[0-9]{1,3}$/', $_SERVER['HTTP_X_REAL_IP'])) {
        $ip = $_SERVER['HTTP_X_REAL_IP'];
    }
    return $ip;

}
echo real_ip();

?>
向上
下
-4jit_chavan在雅虎點com ¶7年前
searched $_SERVER["REDIRECT_URL"] for a while and noted that it is not mentioned in php documentation page itself. look like this is only generated by apache server(not others) and using   $_SERVER["REQUEST_URI"] will be useful in some cases as mine.
向上
下
-2centurianii在雅虎點Co點英國¶3年前
If you apply redirection in ALL your requests using commands at the Apache virtual host file like:
RewriteEngine On
RewriteCond "%{REQUEST_URI}" "!=/index.php"
RewriteRule "^/(.*)$" "index.php?$1" [NC,NE,L,QSA]
you should expect some deviations in your $_SERVER global.

Say, you send a url of: [hostname here]/a/b?x=1&y=2
which makes Apache to modify to: /index.php?/a/b?x=1&y=2

Now your $_SERVER global contains among others:
'REQUEST_URI' => '/a/b?x=1&y=2', it retains the initial url after the host
'QUERY_STRING' => 'a/b&x=1&y=2', notice how php replaces '?' with '&'
'SCRIPT_NAME' => '/index.php', as it was intended to be.

To test your $_SERVER global:
function serverArray(){
   $arr = array();
   foreach($_SERVER as $key=>$value)
      $arr[] = '&nbsp;&nbsp;&nbsp;\'' . $key . '\' => \'' . (isset($value)? $value : '-') . '\'';
   return @\sort($arr)? '$_SERVER = array(<br />' . implode($arr, ',<br />') . '<br />);' : false;
}
echo serverArray();
向上
下
-3約翰·溫格（Johan Winge） ¶1年前
It should probably be noted that the value of $_SERVER['SERVER_PROTOCOL'] will never contain the substring "HTTPS". Assuming this is a common source of bugs and confusion. Instead, see $_SERVER['HTTPS'].
向上
下
-5lilJoshu ¶2年前
Remember,

Although $_SERVER["REQUEST_METHOD"] is initially built with GET, POST, PUT, HEAD in mind, a server can allow more.

This may be important if you're building a RESTful interfaces that will also use methods such as PATCH and DELETE.

Also important as a security risk as a possible point of injection. In the event of building something acting based on REQUEST_METHOD, it's recommended to put it in a switch statement.

<?php
switch ($_SERVER["REQUEST_METHOD"]){
   case "PUT":
       foo_replace_data();
       break;
   case "POST":
       foo_add_data();
       break;
   case "HEAD";
       foo_set_that_cookie();
       break;
   case "GET":
   default:
      foo_fetch_stuff()
      break;
}

?>

```
## $_GET
```
```
## $_POST
```
```
## $_FILES
```
```
## $_REQUEST
```
```
## $_SESSION
```
```
## $_ENV
```
```
## $_COOKIE
```
```
## $http_response_header
```
```
## $argc
```
```
## $argv
```
```


## Deprecated ==> 不在使用了!!
$php_errormsg
```
```

