# ch01
---
## loop.py
```
loop.py
sum = 0

def show(n):
    print("第 " + str(n) + " 次執行迴圈")
    
for i in range(1,11):
    show(i)
    sum += i
print("1+2+...+10 = " + str(sum))

```
## sum.py
```
a = 12
b = 34
sum = a + b
print("總和 = " + str(sum))
```
# ch02
---
## discount.py
```
money = int(input("請輸入購物金額："))
if(money >= 10000):
    if(money >= 100000):
        print(money * 0.8, end=" 元\n")  #八折
    elif(money >= 50000):
        print(money * 0.85, end=" 元\n")  #八五折
    elif(money >= 30000):
        print(money * 0.9, end=" 元\n")  #九折
    else:
        print(money * 0.95, end=" 元\n")  #九五折
else:
    print(money, end=" 元\n")  #未打折
```
## format.py
```
print("姓名   座號  國文  數學  英文")
print("%3s  %2d   %3d   %3d  %3d" % ("林大明", 1, 100, 87, 79))
print("%3s  %2d   %3d   %3d  %3d" % ("陳阿中", 2, 74, 88, 100))
print("%3s  %2d   %3d   %3d  %3d" % ("張小英", 11, 82, 65, 8))

```
## grade.py
```
score = int(input("請輸入成績："))
if(score) >= 90:
    print("優等")
elif(score) >= 80:
    print("甲等")
elif(score) >= 70:
    print("乙等")
elif(score) >= 60:
    print("丙等")
else:
    print("丁等")
```
## password1.py
```
pw = input("請輸入密碼：")
if(pw=="1234"):
    print("歡迎光臨！")
```
## password2.py
```
pw = input("請輸入密碼：")
if(pw=="1234"):
    print("歡迎光臨！")
else:
    print("密碼錯誤！")
```
## score.py
```
nat = input("請輸入國文成績：")
math = input("請輸入數學成績：")
eng = input("請輸入英文成績：")
sum = int(nat) + int(math) + int(eng)  #輸入值需轉換為整數
average = sum / 3
print("成績總分：%d，平均成績：%5.2f" % (sum, average))
```
# ch03
---
## append1.py
```
score = []
total = inscore = 0
while(inscore != -1):
    inscore = int(input("請輸入學生的成績："))
    score.append(inscore)
print("共有 %d 位學生" % (len(score) - 1))
for i in range(0, len(score) - 1):
    total += score[i]
average = total / (len(score) - 1)
print("本班總成績：%d 分，平均成績：%5.2f 分" % (total, average))
```
## floor.py
```
n = int(input("請輸入大樓的樓層數："))
print("本大樓具有的樓層為：")
if(n > 3):
    n += 1
for i in range(1, n+1):
    if(i==4):
        continue
    print(i, end=" ")
print()
```
## list1.py
```
score = [85, 79, 93]
print("國文成績：%d 分" % score[0])
print("數學成績：%d 分" % score[1])
print("英文成績：%d 分" % score[2])
```
## ninenine.py
```
for i in range(1,10):
    for j in range(1,10):
        product = i * j
        print("%d*%d=%-2d   " % (i, j, product), end="")
    print()

```
## numtotal.py
```
sum = 0
n = int(input("請輸入正整數："))
for i in range(1, n+1):
    sum += i
print("1 到 %d 的整數和為 %d" % (n, sum))
```
## prime.py
```
n = int(input("請輸入大於 1 的整數："))
if(n == 2):
    print("2 是質數！")
else:
    for i in range(2, n):
        if(n % i == 0):
            print("%d 不是質數！" % n)
            break
    else:
        print("%d 是質數！" % n)
```
## while1.py
```
total = person = score = 0
while(score != -1):
    person += 1
    total += score
    score = int(input("請輸入第 %d 位學生的成績：" % person))
average = total / (person - 1)
print("本班總成績：%d 分，平均成績：%5.2f 分" % (total, average))
```
# ch04
---
## dictget.py
```
dict1 = {"A":"內向穩重", "B":"外向樂觀", "O":"堅強自信", "AB":"聰明自然"}
name = input("輸入要查詢的血型:")
blood = dict1.get(name)
if blood == None:  
    print("沒有「" + name + "」血型！")
else:  
    print(name + " 血型的個性為：" + str(dict1[name]))
```
## in.py
```
dict1 = {"林小明":85, "曾山水":93, "鄭美麗":67}
name = input("輸入學生姓名：")
if name in dict1:  
    print(name + "的成績為 " + str(dict1[name]))
else:  
    score = input("輸入學生分數：")
    dict1[name] = score
    print("字典內容：" + str(dict1))
```
## item.py
```
dict1={"金牌":26, "銀牌":34, "銅牌":30}
item1 = list(dict1.items())
for name, num in item1:
    print("得到的 %s 數目為 %d 面" % (name, num))

```
## keyvalue.py
```
dict1={"金牌":26, "銀牌":34, "銅牌":30}
listkey = list(dict1.keys())
listvalue = list(dict1.values())
for i in range(len(listkey)):
    print("得到的 %s 數目為 %d 面" % (listkey[i], listvalue[i]))
```
# ch05
---
## ctof.py
```
def ctof(c):  #攝氏轉華氏
    f = c * 1.8 + 32
    return f

inputc = float(input("請輸入攝氏溫度："))
print("華氏溫度為：%5.1f 度" % ctof(inputc))
```
## divmod.py
```
person = int(input("請輸入學生人數: "))
apple = int(input("請輸入蘋果總數: "))
ret = divmod(apple, person)
print("每個學生可分得蘋果 " + str(ret[0]) + " 個")
print("蘋果剩餘 " + str(ret[1]) + " 個")
```
## just.py
```
listname = ["林大明", "陳阿中", "張小英"]
listchinese = [100, 74, 82]
listmath = [87, 88, 65]
listenglish = [79, 100, 8]
print("姓名     座號  國文  數學  英文")
for i in range(0,3):
    print(listname[i].ljust(5), str(i+1).rjust(3), str(listchinese[i]).rjust(5), str(listmath[i]).rjust(5), str(listenglish[i]).rjust(5))

```
## randint.py
```
import random as r

while True:
    inkey = input("按任意鍵再按[ENTER]鍵擲骰子，直接按[ENTER]鍵結束:")
    if len(inkey) > 0:
        num = r.randint(1,6)
        print("你擲的骰子點數為：" + str(num))
    else:  
        print("遊戲結束！")
        break
```
## replace.py
```
date1 = "2017-8-23"
date1 = "西元 " + date1
date1 = date1.replace("-", " 年 ", 1)
date1 = date1.replace("-", " 月 ", 1)
date1 += " 日"
print(date1)
```
## sample.py
```
import random as r

list1 = r.sample(range(1,50), 7)
special = list1.pop()
list1.sort()
print("本期大樂透中獎號碼為：", end="")
for i in range(0,6):
    if i == 5:    print(str(list1[i]))
    else:    print(str(list1[i]), end=", ")
print("本期大樂透特別號為：" + str(special))

```
## sorted.py
```
innum = 0
list1 = []
while(innum != -1):
    innum = int(input("請輸入電費 (-1：結束)："))
    list1.append(innum)
list1.pop()
print("共輸入 %d 個數" % len(list1))
print("最多電費為：%d" % max(list1))
print("最少電費為：%d" % min(list1))
print("電費總和為：%d" % sum(list1))
print("電費由大到小排序為：{}".format(sorted(list1, reverse=True)))
```
## startswith.py
```
web = input("請輸入網址：")
if web.startswith("http://") or web.startswith("https://"):
    print("輸入的網址格式正確！")
else:
    print("輸入的網址格式錯誤！")
```
# ch06
---
## glob.cpython-37.pyc
```
```
## copyfile.py
```
import os
cur_path=os.getcwd() # 取得目前路徑  
os.system("cls")  # 清除螢幕
os.system("mkdir dir2")  # 建立 dir2 目錄
os.system("copy ossystem.py dir2\copyfile.py") # 複製檔案 
file=cur_path + "\dir2\copyfile.py" 
os.system("notepad " + file)  # 以記事本開啟 copyfile.py 檔
```
## test_file.py
```
'''
模式有

r - 讀取(檔案需存在)

w - 新建檔案寫入(檔案可不存在，若存在則清空)

a - 資料附加到舊檔案後面(游標指在EOF)
'''

f = open('A.txt', 'a', encoding = 'UTF-8')   # 也可使用指定路徑等方式，如： C:\A.txt
f.write('你好1\n')
f.write('你好2\n')
f.write('你好3\n')
f.close()


'''
Hello world
Today id a nice day!
'''


f=open('test_file.txt')
print(f.readline())
print(f.readline())
#f.close()


f.seek(0)
for line in f:
    print(line.strip())
    
f.close()

with open("test_file.txt") as f:
    for line in f:
        print(line.strip())          

# write to test_write.txt
# Write a file
with open("test_write.txt", "w") as out_file:
    out_file.write("This Text is going to out file\nLook at it and see!")

```
## oswalk.py
```
import os
cur_path=os.path.dirname(__file__) # 取得目前路徑
sample_tree=os.walk(cur_path)
for dirname,subdir,files in sample_tree:
    print("檔案路徑：",dirname)
    print("目錄串列：" , subdir)   
    print("檔案串列：",files)
    print()
```
## binaryread.py
```
with open('file.bin','rb') as f:
    content=f.read().decode("utf-8") 
    print(content) 
    
```
## binarywrite.py
```
content='''Hello Python
中文字測試
Welcome
'''

content=content.encode("utf-8") #轉成 bytes
with open('file.bin','wb') as f:
    f.write(content)
```
## copytree.py
```
import shutil
shutil.copytree("oswalk","D:\\newoswalk" )  # 目錄複製
```
## fileread1.py
```
f=open('file1.txt','rt')
for line in f:
    print(line,end="")
f.close()
```
## fileread2.py
```
with open('file1.txt','r') as f:
    for line in f:
        print(line,end="")
```
## fileread3.py
```
with open('file1.txt','r') as f:
    str1=f.read(5)
    print(str1)  # Hello
```
## fileread4.py
```
with open('file2.txt','r',encoding ='UTF-8') as f:
    print(f.readline())  # 123中文字\n
    print(f.readline(3)) # abc
```
## fileread5.py
```
with open('file1.txt','r') as f:
    content=f.readlines() 
    print(type(content))   # <class 'list'>
    print(content)  
```
## fileread6.py
```
with open('file2.txt','r',encoding ='UTF-8') as f:
    doc=f.readlines() 
    print(doc)      
    
with open('file2.txt','r',encoding ='UTF-8') as f:
    str1=f.read(5)
    print(str1)  # 123中
```
## fileread7.py
```
with open('file2.txt','r',encoding ='UTF-8-sig') as f:
    doc=f.readlines() 
    print(doc)      
    
with open('file2.txt','r',encoding ='UTF-8-sig') as f:
    str1=f.read(5)
    print(str1)  # 123中文
```
## filereadUTF-8.py
```
f=open('file2.txt','r',encoding ='cp950')
for line in f:
    print(line,end="")
f.close()
```
## fileseek.py
```
# file.bin 內容
'''Hello Python
中文字測試
Welcome
'''

f=open('file.bin','rb')
print("目前文件索引位置：",f.tell()) #0
f.seek(6) #移到索引第 6 (第7個字元)位置
str1=f.read(7) #讀取 7 個字元
print(str1)  # b'Python\n'
print("目前文件索引位置：",f.tell()) #13

f.seek(0) #回文件最前端
print("目前文件索引位置：",f.tell()) #0
str2=f.read(5) #讀取 5 個字元
print(str2)  # b'Hello'

f.seek(-8,2) #移至最尾端，向前取 8 個字元
str3=f.read()
print(str3)  # b'Welcome\n'

f.close()
```
## filewrite1.py
```
content='''Hello Python
中文字測試
Welcome
'''

f=open('file1.txt','w')
f.write(content)
f.close()
```
## glob.py
```
import glob
files = glob.glob("glob.py") + glob.glob("os*.py") + glob.glob("*.txt") 
for file in files:
    print(file)
```
## newfile.py
```
import os,shutil
cur_path=os.path.dirname(__file__) # 取得目前路徑
destfile= cur_path + "\\" + "newfile.py"
shutil.copy("shutil.py",destfile )  # 檔案複製
shutil.copyfile("shutil.py","D:\\new.py" )  # 檔案複製
```
## osdirname.py
```
import os
cur_path=os.path.dirname(__file__) # 取得目前目錄路徑
print("現在目錄路徑："+cur_path)
```
## osexists.py
```
import os
filename=os.path.abspath("osexists.py")
if os.path.exists(filename): #檢查檔案是否存在
    print("完整路徑名稱：" + filename)
    print("檔案大小：" , os.path.getsize(filename))
```
## osgetcwd.py
```
import os

print(os.getcwd())   
 
```
## osmkdir.py
```
import os
dir = "myDir"
if not os.path.exists(dir):
    os.mkdir(dir)
else:
    print(dir + "已經存在!")   
 
```
## ospath.py
```
import os
filename=os.path.abspath("ospath.py")
if os.path.exists(filename):   
    basename=os.path.basename(filename)
    print("最後的檔案或路徑名稱：" + basename)
    
    dirname=os.path.dirname(filename)
    print("目前檔案目錄路徑：" + dirname) 
    
    print("是否為目錄：",os.path.isdir(filename))
    
    fullpath,fname=os.path.split(filename)
    print("目錄路徑：" + fullpath)
    print("檔名：" + fname)
    
    Drive,fpath=os.path.splitdrive(filename)
    print("磁碟機：" + Drive)
    print("路徑名稱：" + fpath)   
    
    fullpath = os.path.join(fullpath + "\\" + fname)
    print("組合路徑= " + fullpath)
```
## osremove.py
```
import os
file = "myFile.txt"
if os.path.exists(file):
    os.remove(file)
else:
    print(file + "檔案未建立!")   
 
```
## osrmdir.py
```
import os
dir = "myDir"
if os.path.exists(dir):
    os.rmdir(dir)
else:
    print(dir + "目錄未建立!")  
 
```
## ossystem.py
```
import os
cur_path=os.getcwd() # 取得目前路徑  
os.system("cls")  # 清除螢幕
os.system("mkdir dir2")  # 建立 dir2 目錄
os.system("copy ossystem.py dir2\copyfile.py") # 複製檔案 
file=cur_path + "\dir2\copyfile.py" 
os.system("notepad " + file)  # 以記事本開啟 copyfile.py 檔
```
## password.py
```
#import ast
import json
data = dict()
with open('password.txt','r', encoding = 'UTF-8-sig') as f:
   filedata = f.read()
   print(filedata)
#   filedata = filedata.replace("\'", "\"")
#   data = ast.literal_eval(filedata)
   data = json.loads(filedata)
print(type(data),data)
```
## rmtree.py
```
import shutil
shutil.rmtree("D:\\newoswalk" )  # 刪除目錄
```
## shutil.py
```
import os,shutil
cur_path=os.path.dirname(__file__) # 取得目前路徑
destfile= cur_path + "\\" + "newfile.py"
shutil.copy("shutil.py",destfile )  # 檔案複製
shutil.copyfile("shutil.py","D:\\new.py" )  # 檔案複製
```
# ch07
---
## __pycache__
```
calculate.cpython-37.pyc
```
## projectArea
---
### projectArea
#### spyproject
#### areapackage
```
from areapackage.myClass import Triangle

triangle = Triangle(5,6) #建立 triangle 物件
print("矩形面積=",triangle.area())    #30
print("三角形面積=",triangle.area2()) #15
```
---
#### areapackage
##### __init__.py
```
# -*- coding: utf-8 -*-
```
##### myClass.py
```
class Rectangle():       #定義父類別  
    def __init__(self, width,height):
        self.width = width    #定義共用屬性   
        self.height = height  #定義共用屬性
    def area(self):           #定義共用方法 
        return self.width * self.height
        
class Triangle(Rectangle): #定義子類別  
    def area2(self):       #定義子類別的共用方法 
        return (self.width * self.height)/2
```
---
## projectArea2
---
#### index.py
```
from areapackage2.Rectangle import Rectangle
from areapackage2.Triangle import Triangle

triangle = Triangle(5,6) #建立 triangle 物件
print("矩形面積=",triangle.area())    #30
print("三角形面積=",triangle.area2()) #15.0
```
### .spyproject
---
### areapackage2
#### __pycache__
##### __init__.py
```
# -*- coding: utf-8 -*-
```
##### Rectangle.py
```
class Rectangle():       #定義父類別  
    def __init__(self, width,height):
        self.width = width    #定義共用屬性   
        self.height = height  #定義共用屬性
    def area(self):           #定義共用方法 
        return self.width * self.height
```
##### Triangle.py
```
from areapackage2.Rectangle import Rectangle
        
class Triangle(Rectangle): #定義子類別  
    def area2(self):       #定義子類別的共用方法 
        return (self.width * self.height)/2
```
---














































