## 示例說明
```
該<!DOCTYPE html>聲明定義，這個文件是一個HTML5文檔

所述<html>元件是一個HTML頁面的根元素

該<head>元素包含HTML頁面的元信息

的<title>元素指定用於HTML頁面的標題（其在瀏覽器的標題欄或在頁面的選項卡顯示）

該<body>元素定義了文檔的身體，並且對於所有的可見內容，諸如標題，段落，圖像，超鏈接，表格，列表等的容器

該<h1>元素定義了一個大的標題

該<p>元素定義了一個段落

```
# 什麼是HTML元素？
```
HTML元素由開始標籤，一些內容和結束標籤定義：

<標記名>內容在這裡... < /標記名>
HTML元素是從開始標記到結束標記的所有內容：

< h1 >我的第一個標題< / h1 >
< p >我的第一段。< / p >


Start tag	     Element content	   End tag

<h1>	         My First Heading	     </h1>

<p>	          My first paragraph.	    </p>

<br>	             none	              none

```
## 注意：
```
某些HTML元素沒有內容（例如<Br>元素）。這些元素稱為空元素。空元素沒有結束標籤！
```
# HTML基本範例
```
所有HTML文檔都必須以文檔類型聲明：開頭<!DOCTYPE html>。

HTML文檔本身以開頭<html>和結尾</html>。

HTML文檔的可見部分在<body>和之間</body>。

例子
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```
# <！DOCTYPE>聲明
```
該<!DOCTYPE>聲明代表文檔類型，並有助於瀏覽器正確顯示網頁。

它只能在頁面頂部（在任何HTML標記之前）出現一次。

該<!DOCTYPE>聲明不區分大小寫。

<!DOCTYPE>HTML5的聲明為：

<!DOCTYPE html>
```
# HTML標題
```
HTML標題是使用<h1>to<h6>標記定義的。

<h1>定義最重要的標題。<h6>定義了最不重要的標題： 

例子
<h1>This is heading 1</h1>
<h2>This is heading 2</h2>
<h3>This is heading 3</h3>
```
# HTML元素
```
HTML元素

HTML元素是從開始標記到結束標記的所有內容：

<標記名>內容在這裡... < /標記名>

一些HTML元素的示例：

< h1 >我的第一個標題< / h1 >

< p >我的第一段。< / p >
```
# HTML屬性
```
HTML屬性

所有HTML元素都可以具有屬性

屬性提供有關元素的其他信息

屬性始終在開始標籤中指定

屬性通常以名稱/值對的形式出現，例如：name =“ value”

```
# href屬性
```
該<a>標籤定義的超鏈接。該 href屬性指定鏈接轉到的頁面的URL：

例子

<a href="https://www.w3schools.com">Visit W3Schools</a>
```
# src屬性
```
該<img>標籤是用來嵌入圖像中的HTML頁面。該src屬性指定要顯示的圖像的路徑：

例子

<img src="img_girl.jpg">
---------------------------------------------------------------------

有兩種方法可以在src 屬性中指定URL ：

1.絕對URL-鏈接到另一個網站上託管的外部圖像。例如：src =“ https://www.w3schools.com/images/img_girl.jpg”。

注意：外部圖像可能受版權保護。如果您未獲得使用許可，則可能違反版權法。此外，您無法控制外部圖像；它可以突然被刪除或更改。

2.相對URL-鏈接到網站內託管的圖像。在此，URL不包含域名。如果URL開頭沒有斜杠，則它將相對於當前頁面。例如：src =“ img_girl.jpg”。如果URL以斜杠開頭，則它將相對於域。例如：src =“ / images / img_girl.jpg”。

提示：幾乎總是最好使用相對URL。如果您更改域，它們不會中斷。
```
# 寬度和高度屬性
```
所述<img>標籤還應該包含 width和 height屬性，用於指定圖像的寬度和高度（以像素為單位）：

例子

<img src="img_girl.jpg" width="500" height="600">
```
# alt屬性
```
如果由於某種原因而無法顯示圖像，則標記的requiredalt屬性<img>指定圖像的備用文本。這可能是由於連接緩慢，src屬性錯誤或用戶使用屏幕閱讀器引起的。

例子

<img src="img_girl.jpg" alt="Girl with a jacket">

Girl with a jacket

If we try to display an image that does not exist, the value of the alt attribute will be displayed instead.
```
# 樣式屬性
```
該style屬性用於向元素添加樣式，例如顏色，字體，大小等。

例子

<p style="color:red;">This is a red paragraph.</p>
```
# lang屬性
```
您應該始終lang在<html>標籤內包含屬性，以聲明網頁的語言。這旨在協助搜索引擎和瀏覽器。

下面的示例將英語指定為語言：

<!DOCTYPE html>

<html lang="en">

<body>
...

</body>

</html>

國家/地區代碼也可以添加到lang 屬性中的語言代碼中。因此，前兩個字符定義HTML頁面的語言，後兩個字符定義國家/地區。

下面的示例將英語指定為語言，將美國指定為國家：

<!DOCTYPE html>

<html lang="en-US">

<body>
...
</body>

</html>
```
## 標題屬性
```
該title屬性定義有關元素的一些額外信息。

當您將鼠標懸停在元素上時，title屬性的值將顯示為工具提示：

例子

<p title="I'm a tooltip">This is a paragraph.</p>
----------------------------------------------------------
我們建議：始終使用小寫屬性

HTML標準不需要小寫的屬性名稱。

title屬性（以及所有其他屬性）可以使用大寫或小寫形式，例如title或TITLE。

但是，W3C建議在HTML中使用小寫字母屬性，而 對於更嚴格的文檔類型（例如XHTML）則要求使用小寫字母屬性。

------------------------------------------
在W3Schools中，我們始終使用小寫的屬性名稱。
------------------------------------------

我們建議：始終引用屬性值

HTML標準不需要在屬性值兩邊加上引號。

但是，W3C建議使用HTML引號，並要求對更嚴格的文檔類型（例如XHTML）進行引號。

好的：

<a href="https://www.w3schools.com/html/">Visit our HTML tutorial</a>

壞的：

<a href=https://www.w3schools.com/html/>Visit our HTML tutorial</a>

```
# 單引號還是雙引號？
```
在HTML中，屬性值周圍的雙引號是最常見的，但是也可以使用單引號。

在某些情況下，當屬性值本身包含雙引號時，有必要使用單引號：

<p title='John "ShotGun" Nelson'>

或相反亦然：

<p title="John 'ShotGun' Nelson">
```
# 章節總結
```
所有HTML元素都可以具有屬性

的href屬性 <a>指定鏈接轉到的頁面的URL

的src屬性 <img>指定要顯示的圖像的路徑

的width和height屬性<img>提供圖片的尺寸信息

的alt屬性 <img>提供圖像的備用文本

該style屬性用於向元素添加樣式，例如顏色，字體，大小等。

標籤的lang屬性<html>聲明網頁的語言

該title屬性定義有關元素的一些額外信息

```
