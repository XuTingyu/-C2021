```
<!DOCTYPE HTML >

<html>

  <head>

    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">

    <title>應用addcslashes()函數和stripslashes()函數分別對字串進行轉義和還原</title>

  </head>

  <body>

    <?php

      $str = "select * from tb_book where bookname = 'PHP5從入門到放棄'";

      echo $str."<br>";

      $a = addslashes($str);  //對字串中的特殊字元進行轉義

      echo $a."<br>"; //輸出轉義後的字元

      $b = stripslashes($a); //對轉義後的字元進行還原

      echo $b."<br>"; //將字元原義輸出

    ?>

  </body>

</html>

說明上述程式stripslashes()與addslashes()
```
```
執行結果:
select * from tb_book where bookname = 'PHP5從入門到放棄'
select * from tb_book where bookname = \'PHP5從入門到放棄\'
select * from tb_book where bookname = 'PHP5從入門到放棄'
```
```
addslashes()
https://www.webtech.tw/info.php?tid=PHP_addslashes_%E5%87%BD%E6%95%B8%E6%9B%BF%E5%AD%97%E7%AC%A6%E5%A2%9E%E5%8A%A0%E6%96%9C%E7%B7%9A
https://www.php.net/manual/en/function.addslashes.php

stripslashes()
https://www.webtech.tw/info.php?tid=PHP_stripslashes_%E5%87%BD%E6%95%B8
https://www.php.net/manual/en/function.stripslashes.php
```
```
addslashes ( string $string ) : string
功能是替字串的特殊字符增加反斜線效果

特殊字符是：
單引號(')
雙引號(")
反斜杠(\)
NULL

會有這樣的需求主要在於部份的特殊符號會造成資料庫的錯誤或資料被竊取，所謂的 sql injection 這種攻擊手法就會用一些特殊符號來偷撈資料
所以一般會用 PHP addslashes 函數來協助避免，讓特殊符號跳脫掉，等於是失效
與 addslashes 函數相對的是用來移除反斜線的 stripslashes 函數。


stripslashes ( string $string ) : string
功能是用來去除字串中多餘的反斜線（\）
1.用來過濾網頁上的資料
2.用來還原 addslashes 函數處理過的字串
```
