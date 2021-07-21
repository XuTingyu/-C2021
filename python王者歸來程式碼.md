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
## projectHello
### .spyproject
### mypackage
### index.py
```
from mypackage.Hello import sayHello

sayHello()
```
#### mypackage
##### __pycache__
---
##### __init__.py
```
# -*- coding: utf-8 -*-
```
##### Hello.py
```
def sayHello():
    print("Hello")
```
---
## Area.py
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
     
triangle = Triangle(5,6) #建立 triangle 物件
print("矩形面積=",triangle.area())    #30
print("三角形面積=",triangle.area2()) #15
```
## calculate.py
```
def add(n1,n2):
    return n1+n2
    
def sub(n1,n2):
    return n1-n2
```
## CallModule.py
```
from areapackage2.Rectangle import Rectangle
from areapackage2.Triangle import Triangle

triangle = Triangle(5,6) #建立 triangle 物件
print("矩形面積=",triangle.area())    #30
print("三角形面積=",triangle.area2()) #15.0
```
## class01.py
```
class Animal():      #定義類別
    name = "小鳥"    #定義屬性
    def sing(self):  #定義方法
        print("很會唱歌!")     
        
bird = Animal()  #以 Animal 類別，建立一個名叫小鳥的 bird物件
print(bird.name) #小鳥
bird.sing()      #很會唱歌!
```
## class02.py
```
class Animal():      #定義類別  
    def __init__(self, name):
        self.name = name  #定義屬性   
    def sing(self):       #定義方法        
        print(self.name + "，很會唱歌!")     
        
bird = Animal("鸚鵡")  #以 Animal 類別，建立一個名叫鸚鵡的 bird物件
print(bird.name) #鸚鵡
bird.sing()      #鸚鵡，很會唱歌!
```
## class03.py
```
class Animal():      #定義類別  
    def __init__(self, name,age):
        self.name = name  #定義屬性 
        self.age = age
    def sing(self):       #定義方法        
        print(self.name + str(self.age) + "歲，很會唱歌!")  
    def grow(self,year):  #定義方法        
        self.age += year     
        
bird = Animal("鸚鵡",1) #以 Animal 類別，建立一個名叫鸚鵡、1歲大的 bird物件
bird.grow(1)     #長大1歲
bird.sing()      #鸚鵡2歲，很會唱歌!
```
## class04.py
```
class Animal():      #定義類別  
    def __init__(self, name,age):
        self.__name = name  #定義私用屬性 
        self.__age = age
    def __sing(self):       #定義私用方法        
        print(self.__name + str(self.__age),end= "歲，很會唱歌，")  
    def talk(self):        #定義共用方法 
        self.__sing()      #使用私用方法
        print("也會模仿人類說話!")
        
bird = Animal("灰鸚鵡",2) #以 Animal 類別，建立一個名叫灰鸚鵡、2歲大的 bird物件
bird.talk()       #灰鸚鵡2歲，很會唱歌，也會模仿人類說話!

bird.__age = -1  #設定無效
bird.talk()      #灰鸚鵡2歲，很會唱歌，也會模仿人類說話!
#bird.__sing()   #執行出現錯誤
```
## class05.py
```
class Animal():      #定義父類別  
    def __init__(self, name):
        self.name = name  #定義共用屬性         
    def fly(self):        #定義共用方法 
        print(self.name + "很會飛!")
        
class Bird(Animal):      #定義子類別  
    def __init__(self, name):
        self.name = "粉紅色" + name  #覆寫父類別的建構式         
    def sing(self):       #定義子類別的方法 
        print(self.name + "也愛唱歌!")        

pigeon = Animal("小白鴿")#以 Animal 類別，建立一個名叫小白鴿的 pigeon 物件
pigeon.fly()  #小白鴿很會飛!
      
parrot = Bird("小鸚鵡")  #以 Bird 類別，建立一個名叫小鸚鵡的 parrot 物件
parrot.fly()  #粉紅色小鸚鵡很會飛!
parrot.sing() #粉紅色小鸚鵡也愛唱歌!
```
## class06.py
```
class Animal():      #定義父類別  
    def __init__(self,name):
        self.name = name  #定義共用屬性         
    def fly(self):        #定義共用方法 
        print(self.name + "很會飛!")
        
class Bird(Animal):      #定義子類別  
    def __init__(self,name,age):
        super().__init__(name) #執行父類別的 __init__()方法
        self.age = age   #定義子類別共用屬性 
    def fly(self):       #定義子類別共用方法         
        print(str(self.age),end="歲") 
        super().fly() #執行父類別的 fly方法

pigeon = Animal("小白鴿") #以 Animal 類別，建立一個名叫小白鴿的 pigeon 物件
pigeon.fly()  #小白鴿很會飛!
      
parrot = Bird("小鸚鵡",2) #以 Bird 類別，建立一個名叫小鸚鵡、2歲大的 parrot 物件
parrot.fly()  #2歲小鸚鵡很會飛!
```
## class07.py
```
class Animal():          #定義父類別         
    def fly(self):       #定義共用方法 
        print("時速 20公里!")
        
class Bird(Animal):      #定義子類別  
    def fly(self,speed): #定義共用方法         
        print("時速 " + str(speed) + "公里!")
        
class Plane():           #定義類別  
    def fly(self):       #定義共用方法         
        print("時速 1000公里!")
        
def fly(speed):          #定義函式         
    print("時速 " + str(speed) + "英哩!")    
        
animal = Animal() #以 Animal 類別建立 animal 物件
animal.fly()  #時速 20公里!
      
bird = Bird() #以 Bird 類別建立 bird 物件
bird.fly(60)  #時速 60公里!

plane=Plane() #以 Plane 類別建立 plane 物件
plane.fly()   #時速 1000公里!

fly(5)        #時速 5英哩!
```
## class08.py
```
class Father():         #定義父類別         
    def say(self):      #定義共用方法 
        print("明天會更好!")
        
class Mother():         #定義父類別  
    def say(self):      #定義共用方法 
        print("包容、尊重!")
        
class Child(Father,Mother): #定義子類別  
    pass
        
child = Child() #建立 child 物件
child.say()     #明天會更好! 
```
## getPrivateAttribute.py
```
class Father():      #定義父類別  
    def __init__(self,name):
        self.name = name    
        self.__eye="黑色" #定義私用屬性
    def getEye(self):    #定義共用方法傳回私用屬性
        return self.__eye
        
class Child(Father):      #定義子類別  
    def __init__(self,name,eye):
        super().__init__(name)
        self.eye=eye
        self.fatherEye=super().getEye() #取得私用屬性
      
joe = Child("小華","棕色") #建立子類別物件 joe
print(joe.name+"眼睛是"+joe.eye+"，他的父親則是"+joe.fatherEye)
# 執行結果：小華眼睛是棕色，他的父親則是黑色      
```
## module-1.py
```
def add(n1,n2):
    return n1+n2
    
def sub(n1,n2):
    return n1-n2

print(add(5,2))  # 7
print(sub(5,2))  # 3
```
## module-2.py
```
import calculate  # 匯入 calculate 模組

print(calculate.add(5,2))  # 7
print(calculate.sub(5,2))  # 3
```
## module-3.py
```
from calculate import add,sub

print(add(5,2))  # 7
print(sub(5,2))  # 3
```
## module-4.py
```
from calculate import add

print(add(5,2))  # 7
print(sub(5,2))  # NameError: name 'sub' is not defined
```
## module-5.py 
```
from calculate import *

print(add(5,2))  # 7
print(sub(5,2))  # 3
```
## module-6.py
```
from calculate import add as a

print(a(5,2))  # 7
```
## module-7.py
```
import calculate as cal # 匯入 calculate 模組，並取別名為 cal

print(cal.add(5,2))  # 7
print(cal.sub(5,2))  # 3
```
## password.py
```
import msvcrt
def pwd_input():  
    chars = [] 
    while True:
        try:
            newChar = msvcrt.getch().decode(encoding="utf-8")
        except:
            return input("請在cmd命令行下執行，否則密碼輸入將無法隱藏:")
        if newChar in '\r\n': # 如果是換行，结束輸入             
             break 
        elif newChar == '\b': # 如果是退格，删除密碼末尾一位並且删除一個星號
             if chars:  
                 del chars[-1] 
                 msvcrt.putch('\b'.encode(encoding='utf-8')) # 游標退回一格
                 msvcrt.putch( ' '.encode(encoding='utf-8')) # 输出一個空格覆蓋原來的星號
                 msvcrt.putch('\b'.encode(encoding='utf-8')) # 游標退回一格準備接受新的输入                 
        else:
            chars.append(newChar)
            msvcrt.putch('*'.encode(encoding='utf-8')) # 顯示 * 號
    return (''.join(chars) )
```
# ch08
---
## Assert.py
```
class Car(): 
    def __init__(self, speed):
        self.speed = speed
        
    def Turbo(self,n):  #增加速度 n      
        assert speed >= 0, '速度不可能為負!'
        self.speed += n

for speed in (60,-20):         
    bus=Car(speed)
    print("初速=",bus.speed,end=" ")
    bus.Turbo(50) 
    print("加速後，速度=",bus.speed)        
```
## div.py
```
def div(a,b):
    return a/b

print(div(6,2))  # 3.0
print(div(3,0)) #中止程式
print(div(4,2))  #未被執行
```
## raise1.py
```
def CheckSpeed(speed): #檢查速度
    if speed < 70:
        raise Exception("速度太慢了!") # 拋出 Exception 型別例外
    if speed > 110:
        raise Exception("已經超速了!") # 拋出 Exception 型別例外 

for speed in (60,100,150):       
    try:
        CheckSpeed(speed) #檢查速度
    except Exception as e: #接收 Exception的例外
        print("現在速度：{}，{}" .format(speed,e))
    else:
        print("目前時速：{}" .format(speed))
```
## raise2.py
```
class MyException(RuntimeError):
    def __init__(self, arg):
        self.args = arg

def CheckSpeed(speed): #檢查速度
    if speed < 70:
        raise Exception("速度太慢了!") # 拋出 Exception 型別例外
    if speed > 110:
        raise Exception("已經超速了!") # 拋出 Exception 型別例外
    else:
        raise MyException("快樂駕駛，平安返家!") # 拋出 MyException 型別例外 
        
def convertTuple(tup):  # tuple 轉換為字串
    str =  ''.join(tup) 
    return str        
 
for speed in (60,100,150):      
    try:
        CheckSpeed(speed) #檢查速度
    except MyException as e: #接收 MyException 的例外
        err= convertTuple(e.args) # tuple 轉換為串字
        print("目前時速：{}，{}" .format(speed,err))    
    except Exception as e: #接收 Exception 的例外
        print("現在速度：{}，{}" .format(speed,e))   
```
## Traceback.py
```
import traceback

def CheckSpeed(speed): #檢查速度
    if speed < 70:
        raise Exception("速度太慢了!") # 拋出 Exception 型別例外
    if speed > 110:
        raise Exception("已經超速了!") # 拋出 Exception 型別例外 

for speed in (60,100,150):       
    try:
        CheckSpeed(speed) #檢查速度
    except Exception as e: #接收 Exception的例外
        with open("err.txt","a") as f:
            f.write(traceback.format_exc()) #寫入例外過程
        print("錯誤資訊寫入完成!")
    else:
        print("目前時速：{}" .format(speed))  
```
## try1.py
```
try:
    print(n)
except:
    print("變數 n 不存在!")  
```
## try2.py
```
n=2
try:
    n+=1
except:
    print("變數 n 不存在!")
else:
    print("n=",n) # n=3
```
## try3.py
```
try:
    print(n)
except Exception as e:
    print(e) 
```
## try4.py
```
try:
    print(n)
except:
    print("變數 n 不存在!")
finally:
    print("一定會執行的程式區塊")    
```
## tryadd.py
```
try:
    a=int(input("請輸入第一個整數："))
    b=int(input("請輸入第二個整數："))
    r = a + b
    print("r=",r)
except:
    print("發生輸入非數值的錯誤!") 
```
## trymod.py
```
try:
    a=int(input("請輸入第一個整數："))
    b=int(input("請輸入第二個整數："))
    r = a % b    
except ValueError:
    print("發生輸入非數值的錯誤!")   
except Exception as e:
    print("發生",e,"的錯誤，包括分母為 0 的錯誤!")
else:
    print("r=",r)
finally:
    print("一定會執行的程式區塊")    
```
## trymod2.py
```
try:
    a=int(input("請輸入第一個整數："))
    b=int(input("請輸入第二個整數："))
    r = a % b    
except(ValueError,ZeroDivisionError):
    print("發生輸入非數值的錯誤或分母為 0 的錯誤!")   
else:
    print("r=",r)
```
## trymod3.py
```
try:
    a=int(input("請輸入第一個整數："))
    b=int(input("請輸入第二個整數："))
    r = a % b    
except(ValueError,ZeroDivisionError) as e:
    print("發生{} 0 的錯誤!" .format(e))   
else:
    print("r=",r)
```
# ch09
---
## eword_tkinter.py
```
def First():  # 首頁
    global page
    page=0
    disp_data()
 
def Prev():  #上一頁
    global page
    if page>0:
        page -=1
        disp_data()     
       
def Next(): #下一頁
    global page
    if page<pagesize:
        page +=1
        disp_data()
    
def Bottom(): #最後頁
    global page
    page=pagesize    
    disp_data() 

def disp_data():
    if datas != None:          
        sep1=tk.Label(frameShow, text="\t",fg="white",width="20",font=("新細明體",10))       
        label1 = tk.Label(frameShow, text="單字".ljust(30),fg="white",bg="black",width=30,font=("新細明體",10))
        label2 = tk.Label(frameShow, text="中文翻譯".ljust(175),fg="white",bg="black",width=80,font=("新細明體",10))
        sep1.grid(row=0,column=0,sticky="w")  # 加第一列空白，讓版面美觀些   
        label1.grid(row=1,column=0,sticky="w")
        label2.grid(row=1,column=1,sticky="w")
        
        n=0   # 資料從索引 0 開始
        row=2 # 資料從第二列開始
        start=page * pagesize + row
        for eword,cword in datas.items():
            # 顯示目前 page頁的資料
            if n >= start and n < start + pagesize: 
                label1 = tk.Label(frameShow, text="\t"+'{0:30}'.format(eword),fg="blue",font=("新細明體",10))
                label2 = tk.Label(frameShow, text='{0:30}'.format(cword),fg="blue",font=("新細明體",10))
                label1.grid(row=row,column=0,sticky="w")
                label2.grid(row=row,column=1,sticky="w")
                row+=1
            n+=1

### 主程式從這裡開始 ###    

import tkinter as tk
import math
win=tk.Tk()
win.geometry("500x300")
win.title("英文單字王")

page,pagesize=0,10
datas=dict()

with open('eword.txt','r', encoding = 'UTF-8-sig') as f:
    for line in f:
        eword,cword = line.rstrip('\n').split(',')
        datas[eword]=cword
print("轉換完畢!") 

datasize=len(datas) #資料筆數
totpage=math.ceil(datasize/pagesize) #總頁數

# 單字顯示區
frameShow = tk.Frame(win)  
frameShow.pack()
labelwords = tk.Label(win, text="")
labelwords.pack() 

frameCommand = tk.Frame(win)  # 翻頁按鈕容器
frameCommand.pack()  
btnFirst = tk.Button(frameCommand, text="第一頁", width=8,command=First)
btnPrev = tk.Button(frameCommand, text="上一頁", width=8,command=Prev)
btnNext = tk.Button(frameCommand, text="下一頁", width=8,command=Next)
btnBottom = tk.Button(frameCommand, text="最末頁", width=8,command=Bottom)
btnFirst.grid(row=0, column=0, padx=5, pady=5)
btnPrev.grid(row=0, column=1, padx=5, pady=5)
btnNext.grid(row=0, column=2, padx=5, pady=5)        
btnBottom.grid(row=0, column=3, padx=5, pady=5)   

First()
win.mainloop()
```
## tk.py
```
import tkinter as tk
win = tk.Tk()
win.geometry("450x100")
win.title("這是主視窗")
win.mainloop()
```
## tkbutton1.py
```
def click1():
    textvar.set("我已經被按過了！")

import tkinter as tk

win = tk.Tk()
textvar = tk.StringVar()
button1 = tk.Button(win, textvariable=textvar, command=click1)
textvar.set("按鈕")
button1.pack()
win.mainloop()
```
## tkbutton2.py
```
def clickme():
    global count
    count += 1
    labeltext.set("你按我 " + str(count) + " 次了！")
    if(btntext.get() == "按我！"):
        btntext.set("回復原來文字！")
    else:
        btntext.set("按我！")

import tkinter as tk

win = tk.Tk()
labeltext = tk.StringVar()
btntext = tk.StringVar()
count = 0
label1 = tk.Label(win, fg="red", textvariable=labeltext)
labeltext.set("歡迎光臨Tkinter！")
label1.pack()
button1 = tk.Button(win, textvariable=btntext, command=clickme)
btntext.set("按我！")
button1.pack()
win.mainloop()
```
## tkcheckbox1.py
```
def choose():
    str = "你喜歡的球類運動："
    for i in range(0, len(choice)):
        if(choice[i].get() == 1):
            str = str + ball[i] + " "
    msg.set(str)

import tkinter as tk

win = tk.Tk()
choice = []
ball = ["足球", "籃球", "棒球"]
msg = tk.StringVar()
label = tk.Label(win, text="選擇喜歡的球類運動：")
label.pack()
for i in range(0, len(ball)):
    tem = tk.IntVar()
    choice.append(tem)
    item = tk.Checkbutton(win, text=ball[i], variable=choice[i], command=choose)
    item.pack()
lblmsg = tk.Label(win, fg="red", textvariable=msg)
lblmsg.pack()
win.mainloop()
```
## tkframe1.py
```
import tkinter as tk
win = tk.Tk()
frame1 = tk.Frame(win)
frame1.pack()
label1=tk.Label(frame1, text="標籤一：")
entry1 = tk.Entry(frame1)
label1.grid(row=0, column=0)
entry1.grid(row=0, column=1)
frame2 = tk.Frame(win)
frame2.pack()
button1 = tk.Button(frame2, text="確定")
button2 = tk.Button(frame2, text="取消")
button1.grid(row=0, column=0)
button2.grid(row=0, column=1)
win.mainloop()
```
## tkgrid1.py
```
import tkinter as tk
win = tk.Tk()
button1 = tk.Button(win, text="這是按鈕一", width=20)
button1.grid(row=0, column=0, padx=5, pady=5)
button2 = tk.Button(win, text="這是按鈕二", width=20)
button2.grid(row=0, column=1, padx=5, pady=5)
button3 = tk.Button(win, text="這是按鈕三", width=20)
button3.grid(row=0, column=2, padx=5, pady=5)
button4 = tk.Button(win, text="這是按鈕四", width=20)
button4.grid(row=1, column=0, padx=5, pady=5)
button5 = tk.Button(win, text="這是按鈕五", width=20)
button5.grid(row=1, column=1, padx=5, pady=5)
button6 = tk.Button(win, text="這是按鈕六", width=20)
button6.grid(row=1, column=2, padx=5, pady=5)
win.mainloop()
```
## tkgrid2.py
```
import tkinter as tk
win = tk.Tk()
button1 = tk.Button(win, text="這是按鈕一", width=20)
button1.grid(row=0, column=0, padx=5, pady=5)
button2 = tk.Button(win, text="這是按鈕二", width=20)
button2.grid(row=0, column=1, padx=5, pady=5, columnspan=2,sticky="e")
button3 = tk.Button(win, text="這是按鈕三", width=20)
button3.grid(row=0, column=3, padx=5, pady=5)
button4 = tk.Button(win, text="這是按鈕四", width=20)
button4.grid(row=1, column=0, padx=5, pady=5)
button5 = tk.Button(win, text="這是按鈕五", width=20)
button5.grid(row=1, column=1, padx=5, pady=5)
button6 = tk.Button(win, text="這是按鈕六", width=20)
button6.grid(row=1, column=2, padx=5, pady=5)
win.mainloop()
```
## tklabel1.py
```
import tkinter as tk
win = tk.Tk()
label1 = tk.Label(win, text="這是標籤元件！", fg="red", bg="yellow", font=("新細明體", 12), padx=20, pady=10)
label1.pack()
win.mainloop()
```
## tkpack1.py
```
import tkinter as tk
win = tk.Tk()
button1 = tk.Button(win, text="這是按鈕一", width=20)
button1.pack()
button2 = tk.Button(win, text="這是按鈕二", width=20)
button2.pack()
button3 = tk.Button(win, text="這是按鈕三", width=20)
button3.pack()
button4 = tk.Button(win, text="這是按鈕四", width=20)
button4.pack()
win.mainloop()
```
## tkpack2.py
```
import tkinter as tk
win = tk.Tk()
button1 = tk.Button(win, text="這是按鈕一", width=20)
button1.pack(padx=20, pady=5)
button2 = tk.Button(win, text="這是按鈕二", width=20)
button2.pack(padx=20, pady=5)
button3 = tk.Button(win, text="這是按鈕三", width=20)
button3.pack(padx=20, pady=5)
button4 = tk.Button(win, text="這是按鈕四", width=20)
button4.pack(padx=20, pady=5)
win.mainloop()
```
## tkpack3.py
```
import tkinter as tk
win = tk.Tk()
button1 = tk.Button(win, text="這是按鈕一", width=20)
button1.pack(padx=20, pady=5, side="right")
button2 = tk.Button(win, text="這是按鈕二", width=20)
button2.pack(padx=20, pady=5, side="left")
button3 = tk.Button(win, text="這是按鈕三", width=20)
button3.pack(padx=20, pady=5, side="bottom")
button4 = tk.Button(win, text="這是按鈕四", width=20)
button4.pack(padx=20, pady=5)
win.mainloop()
```
## tkpassword.py
```
def checkPW():
    if(pw.get() == "1234"):
        msg.set("密碼正確，歡迎登入！")
    else:
        msg.set("密碼錯誤，請修正密碼！")

import tkinter as tk

win = tk.Tk()
pw = tk.StringVar()
msg = tk.StringVar()
label = tk.Label(win, text="請輸入密碼：")
label.pack()
entry = tk.Entry(win, textvariable=pw)
entry.pack()
button = tk.Button(win, text="登入", command=checkPW)
button.pack()
lblmsg = tk.Label(win, fg="red", textvariable=msg)
lblmsg.pack()
win.mainloop()
```
## tkplace1.py
```
import tkinter as tk
win = tk.Tk()
win.geometry("300x100")
label1=tk.Label(win, text="輸入成績：")
label1.place(x=20, y=20)
score = tk.StringVar()
entryUrl = tk.Entry(win, textvariable=score)
entryUrl.place(x=90, y=20)
btnDown = tk.Button(win, text="計算成績")
btnDown.place(x=80, y=50)
win.mainloop()
```
## tkplace2.py
```
import tkinter as tk
win = tk.Tk()
win.geometry("400x150")
button1 = tk.Button(win, text="這是按鈕一", width=20)
button1.place(relx=0.5, rely=0.5, anchor="center")
button2 = tk.Button(win, text="這是按鈕二", width=20)
button2.place(relx=0.1, rely=0.1, anchor="nw")
button3 = tk.Button(win, text="這是按鈕三", width=20)
button3.place(relx=0.1, rely=0.8, anchor="w")
win.mainloop()
```
## tkradio1.py
```
def choose():
    msg.set("你最喜歡的球類運動：" + choice.get())

import tkinter as tk

win = tk.Tk()
choice = tk.StringVar()
msg = tk.StringVar()
label = tk.Label(win, text="選擇最喜歡的球類運動：")
label.pack()
item1 = tk.Radiobutton(win, text="足球", value="足球", variable=choice, command=choose)
item1.pack()
item2 = tk.Radiobutton(win, text="籃球", value="籃球", variable=choice, command=choose)
item2.pack()
item3 = tk.Radiobutton(win, text="棒球", value="棒球", variable=choice, command=choose)
item3.pack()
lblmsg = tk.Label(win, fg="red", textvariable=msg)
lblmsg.pack()
item1.select()
choose()
win.mainloop()
```
## tktext1.py
```
import tkinter as tk
win = tk.Tk()
text = tk.Text(win)
text.insert(tk.INSERT, "Tkinter 套件是圖形使用者介面，\n")
text.insert(tk.INSERT, "雖然功能略為陽春，\n")
text.insert(tk.INSERT, "但已足夠一般應用程式使用，\n")
text.insert(tk.INSERT, "而且是內含於 Python 系統中，\n")
text.insert(tk.END, "不需另外安裝即可使用。")
text.pack()
text.config(state=tk.DISABLED)
win.mainloop()
```
# ch10
---
## bracket.py
```
import re
pat =r'[0-9+]+'
s="Amy was 18 year old,she likes Python and C++."
m = re.findall(pat,s)
print(m) # ['18', '++']
```
## compile.py
```
import re
reobj = re.compile(r'[a-z]+')
m = reobj.findall('3tem12po')
print(m) # ['tem', 'po']
```
## dotall.py
```
import re
pat =r'.*'
s="Do your best,\nGo Go Go!"
m = re.search(pat,s)
print(m.group()) # Do your best,
m2 = re.search(r'.*',s,re.DOTALL)
print(m2.group()) # Do your best,\nGo Go Go!
```
## findall.py
```
import re
pat = re.compile('[a-z]+')
m = pat.findall('tem12po')
print(m)  # ['tem', 'po']
```
## ignore.py
```
import re
pat =r'PYTHON|ANDROID'
s="I like Python and Android!"
m = re.findall(pat,s,re.I)
print(m) #['Python', 'Android']
```
## match.py
```
import re
pat = re.compile(r'[a-z]+')

m = pat.match('tem12po')
print(m) # <re.Match object; span=(0, 3), match='tem'>
if not m==None:
    print(m.group()) #tem
    print(m.start()) #0
    print(m.end())   #3
    print(m.span())  #(0,3)
```
## not1.py
```
import re
pat =r'[^a-z. ]+'
s="John was 18 year old."
m = re.findall(pat,s)
print(m) #['J', '18']
```
## not2.py
```
import re
pat =r'^\d+'
s="2020 is coming soon"
m = re.findall(pat,s)
print(m) #['2020']
m2 = re.findall(r'\w+$',s)
print(m2) #['soon']
```
## phone_check.py
```
def isTaiwanPhone(str):
    if len(str) != 11:       # 如果長度不是11
        return False         # 傳回非手機號碼格式
    #檢查11個字元是否符合手機號碼格式
    for i in range(0, 11):    
        if i==4:
            if str[4] != '-':        # 如果第5個字元不是'-'字元
                return False         # 傳回非手機號碼格式
        else: # 如果前4個字或最後6個字出現非數字字元
            if str[i].isdecimal() == False:
                return False     # 傳回非手機號碼格式
    return True                  # 傳回是正確手機號碼格式        

print("0937-123456 是台灣手機號碼：", isTaiwanPhone('0937-123456'))
print("02-12345678 是台灣手機號碼：", isTaiwanPhone('02-12345678'))
```
## phone1.py
```
import re
numStr="tel:04-12345678"
pat = r'(\d{2})-(\d{8})'

phone = re.search(pat,numStr)
if not phone==None:
    print(phone.group())  #04-12345678
    print(phone.group(0)) #04-12345678
    print(phone.group(1)) #04
    print(phone.group(2)) #12345678   
```
## phone2.py
```
import re
numStr="tel:(04)12345678"
pat = r'(\(\d{2}\))(\d{8})'

phone = re.search(pat,numStr)
if not phone==None:
    print(phone.group())  #(04)12345678
    print(phone.group(1)) #(04)
    print(phone.group(2)) #12345678
```
## phone3.py
```
import re
phoneList=["(04)12345678","(04)-12345678"]
pat = r'(\(\d{2}\))-?(\d{8})'

for phone in phoneList:
    phoneNum = re.search(pat,phone)
    if not phoneNum==None:
        print(phoneNum.group())
```
## phone4.py
```
import re
phoneList=["0412345678","(04)12345678","(04)-12345678","(049)2987654","0937-998877"]
pat = r'\(\d{2,4}\)-?\d{6,8}|\d{9,10}|\d{4}-\d{6,8}'
for phone in phoneList:
    phoneNum = re.search(pat,phone)
    if not phoneNum==None:
        print(phoneNum.group())
```
## plus.py
```
import re
pat = re.compile(r'[aeiou]+')
s="John is my best friend."
m = re.findall(pat,s)
print(m) #['o', 'i', 'e', 'ie']
```
## re_findall.py
```
import re
m = re.findall(r'[a-z]+','tem12po')
print(m)  # ['tem', 'po']
```
## re_match.py
```
import re
pat = r'[a-z]+'
m = re.match(pat,'tem12po')
print(m) # <re.Match object; span=(0, 3), match='tem'>
```
## re_search.py
```
import re
pat = '[a-z]+'
m = re.search(pat,'3tem12po')
print(m) # <re.Match object; span=(1, 4), match='tem'>
```
## re_verbose.py
```
import re
phoneList=["0412345678","(04)12345678","(04)-12345678","(049)2987654","0937-998877"]
pat = r'''
 \(\d{2,4}\)-?\d{6,8} #(04)12345678、(04)-12345678、(049)2987654 等電話格式
|\d{9,10}             #0412345678 等含 9~10 位數字
|\d{4}-\d{6,8}        #0937-998877 等手機格式
'''

for phone in phoneList:
    phoneNum = re.search(pat,phone,re.VERBOSE)
    if not phoneNum==None:
        print(phoneNum.group())
```
## regex.py
```
html = """
<div class="content">
    E-Mail：<a href="mailto:mail@test.com.tw">mail</a><br>
    E-Mail2：<a href="mailto:mail2@test.com.tw">mail2</a><br>
    <ul class="price">定價：360元 </ul>
    <img src="http://test.com.tw/p1.jpg">
    <img src="http://test.com.tw/p2.jpg">
    <img src="http://test.com.tw/p3.png">
    電話：(04)-76543210、0937-123456
</div>
"""

import re

emails = re.findall(r'[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+',html)
for email in emails: #顯示 email
    print(email)

price=re.findall(r'[\d]+元',html)[0].split('元')[0] #價格
print(price) #顯示定價金額

imglist = re.findall(r'[http://]+[a-zA-Z0-9-/.]+\.[jpgpng]+',html)
for img in imglist: #
    print(img) #顯示圖片網址
    
phonelist = re.findall(r'\(?\d{2,4}\)?\-\d{6,8}',html)
for phone in phonelist:
    print(phone) #顯示電話號碼 
```
## search.py
```
import re
pat = re.compile('[a-z]+')

m = pat.search('3tem12po')
print(m) # <re.Match object; span=(1, 4), match='tem'>
if not m==None:
    print(m.group())  # tem
    print(m.start())  # 1
    print(m.end())    # 4
    print(m.span())   # (1,4)
```
## star.py
```
import re
pat = re.compile(r'[aeiou]*')
s="John is my best friend."
m = re.findall(pat,s)
print(m) 
```
## sub1.py
```
import re
pat=r"\d+"
substr="*"
s="Password:1234,ID:5678"
result = re.sub(pat,substr,s)
print(result) # Password:*,ID:*
```
## sub2.py
```
import re

def multiply(m):
    v = int(m.group())
    return str(v * 2)

result = re.sub("\d+", multiply, "10 20 30 40 50",3)
print(result) # 20 40 60 40 50
```
## wild.py
```
import re
pat =r'.o'
s="Do your best!"
m = re.findall(pat,s)
print(m) # ['Do', 'yo']
m2 = re.findall(r'.*o',s)
print(m2) # ['Do yo']
```
# ch11
---
## bs1.py
```
import requests
from bs4 import BeautifulSoup
url = 'http://ehappy.tw/bsdemo1.htm'
html = requests.get(url)
html.encoding = 'UTF-8'
sp = BeautifulSoup(html.text, 'html.parser')

print(sp.title)
print(sp.title.text)
print(sp.h1)
print(sp.p)
```
## bs2.py
```
from bs4 import BeautifulSoup
html = '''
<html>
  <head><meta charset="UTF-8"><title>我是網頁標題</title></head>
  <body>
      <p id="p1">我是段落一</p>
      <p id="p2" class='red'>我是段落二</p>
  </body>
</html>
'''
sp = BeautifulSoup(html, 'html.parser')
print(sp.find('p'))
print(sp.find_all('p'))
print(sp.find('p', {'id':'p2', 'class':'red'}))
print(sp.find('p', id='p2', class_= 'red'))
```
## bs3.py
```
from bs4 import BeautifulSoup
html = '''
<html>
  <head><meta charset="UTF-8"><title>我是網頁標題</title></head>
  <body>
      <p id="p1">我是段落一</p>
      <p id="p2" class='red'>我是段落二</p>
  </body>
</html>
'''
sp = BeautifulSoup(html, 'html.parser')
print(sp.select('title'))
print(sp.select('p'))
print(sp.select('#p1'))
print(sp.select('.red'))
```
## bs4.py
```
from bs4 import BeautifulSoup
html = '''
<html>
  <head><meta charset="UTF-8"><title>我是網頁標題</title></head>
  <body>
      <img src="http://www.ehappy.tw/python.png">
      <a href="http://www.e-happy.com.tw">超連結</a>
  </body>
</html>
'''
sp = BeautifulSoup(html, 'html.parser')
print(sp.select('img')[0].get('src'))
print(sp.select('a')[0].get('href'))
print(sp.select('img')[0]['src'])
print(sp.select('a')[0]['href'])
```
## bs5.py
```
html = """
<html><head><title>網頁標題</title></head>
<h1>文件標題</h1>
<div class="content">
    <div class="item1">
        <a href="http://example.com/one" class="red" id="link1">First</a>
        <a href="http://example.com/two" class="red" id="link2">Second</a>
    </div>
    <a href="http://example.com/three" class="blue" id="link3">
        <img src="http://example.com/three.jpg">Third
    </a>
</div>
"""

from bs4 import BeautifulSoup
sp = BeautifulSoup(html,'html.parser') 

print(sp.title) # <title>網頁標題</title>

print(sp.find('h1')) # <h1>文件標題</h1>

print(sp.find_all('a')) 
print(sp.find_all("a", {"class":"red"}))

data1=sp.find("a", {"href":"http://example.com/one"})
print(data1.text) # First

data2 = sp.select("#link1") 
print(data2[0].text) # First
print(data2[0].get("href")) # http://example.com/one
print(data2[0]["href"])     # http://example.com/one

print(sp.find_all(['title','h1'])) # [<title>網頁標題</title>, <h1>文件標題</h1>]

print(sp.select('div img')[0]['src']) # http://example.com/three.jpg
```
## get.py
```
import requests
url = 'http://www.ehappy.tw/demo.htm'
r = requests.get(url)
# 檢查HTTP回應碼是否為200(requests.code.ok)
if r.status_code == requests.codes.ok:
    print(r.text)
```
## get_cookie.py
```
import requests
url = 'https://www.ptt.cc/bbs/Gossiping/index.html'
# 設定cookies的值
cookies = {'over18':'1'}
r = requests.get(url, cookies=cookies)
print(r.text)
```
## get_headers.py
```
import requests
url = 'https://irs.thsrc.com.tw/IMINT/'
# 自訂表頭
headers={
   'user-agent':'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.186 Safari/537.36'
}
# 將自訂表頭加入 GET 請求中
r = requests.get(url, headers=headers)
print(r)
```
## get_params.py
```
import requests
# 將查詢參數定義為字典資料加入GET請求中
payload = {'key1': 'value1', 'key2': 'value2'}
r = requests.get("http://httpbin.org/get", params=payload)
print(r.text)
```
## iplookup.py
```
import requests
# 設定查詢目前IP的api網址
url = 'https://api.ipify.org'
r = requests.get(url)

print('我目前的IP是：', r.text)
```
## loginFacebook.py
```
from selenium import webdriver
# 設定facebook登入資訊
url = 'https://www.facebook.com/'
email='你的faceook電子郵件'
password='你的faceook密碼'
# 建立瀏覽器物件
driver = webdriver.Chrome()
# 最大化視窗後開啟facebook網站
driver.maximize_window()
driver.get(url)
# 執行自動登入動作
driver.find_element_by_id('email').send_keys(email) #輸入郵件
driver.find_element_by_id('pass').send_keys(password)#輸入密碼
driver.find_element_by_id('loginbutton').click()    # 按登入鈕
```
## post.py
```
import requests
# 將查詢參數加入 POST 請求中
payload = {'key1': 'value1', 'key2': 'value2'}
r = requests.post("http://httpbin.org/post", data=payload)
print(r.text)
```
## taiwanlottery.py
```
import requests
from bs4 import BeautifulSoup
url = 'https://www.taiwanlottery.com.tw/'
r = requests.get(url)
sp = BeautifulSoup(r.text, 'html.parser')
# 找到威力彩的區塊
datas = sp.find('div', class_='contents_box02')
# 開獎期數
title = datas.find('span', 'font_black15').text
print('威力彩期數：', title)
# 開獎號碼
nums = datas.find_all('div', class_='ball_tx ball_green')
# 開出順序
print('開出順序：', end=' ')
for i in range(0,6):
    print(nums[i].text, end=' ')
# 大小順序
print('\n大小順序：', end=' ')
for i in range(6,12):
    print(nums[i].text, end=' ')
# 第二區
num = datas.find('div', class_='ball_red').text
print('\n第二區：', num)
```
# ch12
---
## csv_read.py
```
import csv
# 開啟 csv 檔案
with open('test1.csv', newline='') as csvfile:
    # 讀取 csv 檔案內容
    rows = csv.reader(csvfile)
    
    # 以迴圈顯示每一列
    for row in rows:
        print(row)
```
## csv_read_dict.py
```
import csv
# 開啟 csv 檔案
with open('test1.csv', newline='') as csvfile:
    # 讀取 csv 檔內容，將每一列轉成 dictionary
    rows = csv.DictReader(csvfile)   
    
    # 以迴圈顯示每一列
    for row in rows:
        print(row['姓名'],row['身高'],row['體重'])
```
## csv_write_dict.py
```
import csv
with open('test3.csv', 'w', newline='') as csvfile:
    # 定義欄位
    fieldnames = ['姓名', '身高', '體重']

    # 將 dictionary 寫入 csv 檔
    writer = csv.DictWriter(csvfile, fieldnames=fieldnames)

    # 寫入欄位名稱
    writer.writeheader()
    # 寫入資料
    writer.writerow({'姓名': 'Chiou', '身高': 170, '體重': 65})
    writer.writerow({'姓名': 'David', '身高': 183, '體重': 78})
```
## csv_write_list1.py
```
import csv
# 開啟輸出的 csv 檔案
with open('test1.csv', 'w', newline='') as csvfile:
  # 建立 csv 檔寫入物件
  writer = csv.writer(csvfile)

  # 寫入欄位名稱
  writer.writerow(['姓名', '身高', '體重'])
  # 寫入資料
  writer.writerow(['Chiou', 170, 65])
  writer.writerow(['David', 183, 78])
```
## csv_write_list2.py
```
import csv
# 建立csv二維串列資料
csvtable = [
        ['姓名', '身高', '體重'],
        ['Chiou', 170, 65],
        ['David', 183, 78],
]
# 開啟輸出的 csv 檔案
with open('test2.csv', 'w', newline='') as csvfile:
  # 建立 csv 檔寫入物件
  writer = csv.writer(csvfile)

  # 寫入二維串列資料
  writer.writerows(csvtable)
```
## fetchall.py
```
import sqlite3
conn = sqlite3.connect('test.sqlite') # 建立資料庫連線
cursor = conn.execute('select * from contact')
rows = cursor.fetchall()
# 顯示原始資料
print(rows)
# 逐筆顯示資料
for row in rows:
    print(row[0],row[1])
conn.close()  # 關閉資料庫連線
```
## fetchone.py
```
import sqlite3
conn = sqlite3.connect('test.sqlite') # 建立資料庫連線
cursor = conn.execute('select * from contact')
row = cursor.fetchone()
print(row[0], row[1])

conn.close()  # 關閉資料庫連線
```
## LinkGoogleSheet.py
```
import gspread
from oauth2client.service_account import ServiceAccountCredentials as sac
# 設定金鑰檔路徑及驗證範圍
auth_json = 'PythonConnectGsheet1-6a6086d149c5.json'
gs_scopes = ['https://spreadsheets.google.com/feeds']
# 連線資料表
cr = sac.from_json_keyfile_name(auth_json, gs_scopes)
gs_client = gspread.authorize(cr) 
# 開啟資料表
spreadsheet_key = '1OihpM657yWo1lc3RjskRfZ8m75dCPwL1IPwoDXSvyzI' 
sheet = gs_client.open_by_key(spreadsheet_key)
# 開啟工作簿
wks = sheet.sheet1
# 清除所有內容
wks.clear() 
# 新增列
listtitle=["姓名","電話"]
wks.append_row(listtitle)  # 標題
listdata=["chiou","0937-1234567"]
wks.append_row(listdata)  # 資料內容
```
## mysqldelete.py
```
import pymysql
conn = pymysql.connect('localhost',port=3306,user='root',passwd='1234',charset='utf8', db='pythondb')  #連結資料庫

with conn.cursor() as cursor:
    sql = "delete from scores where ID = 4"
    cursor.execute(sql)
    conn.commit()
    sql = "select * from scores"
    cursor.execute(sql)    
    data = cursor.fetchall()
    print(data)
    
conn.close()
```
## mysqlinsert.py
```
import pymysql
conn = pymysql.connect('localhost',port=3306,user='root',passwd='1234',charset='utf8', db='pythondb')  #連結資料庫

with conn.cursor() as cursor:
    sql = """
    insert into scores (Name, Chinese, English, Math) values 
    ('李大毛',95,92,80),
    ('林小明',82,83,61),
    ('黃小英',74,53,71),
    ('劉大樹',86,87,89),
    ('何美麗',89,73,95)
    """
    cursor.execute(sql)
    conn.commit()  #提交資料庫
conn.close()
```
## mysqlquery.py
```
import pymysql
conn = pymysql.connect('localhost',port=3306,user='root',passwd='1234',charset='utf8', db='pythondb')  #連結資料庫

with conn.cursor() as cursor:
    sql = "select * from scores"
    cursor.execute(sql)
    datas = cursor.fetchall()   # 取出所有資料
    print(datas)
    print('-' * 30)             # 畫分隔線
    sql = "select * from scores"
    cursor.execute(sql)    
    data = cursor.fetchone()    # 取出第一筆資料
    print(data)
    
conn.close()
```
## mysqlselect.py
```
import pymysql

conn = pymysql.connect('localhost',port=3306,user='root',passwd='1234',charset='utf8', db='pythondb')  #連結資料庫
cursor = conn.cursor()

sql1 = "select * from score"  #查詢資料
cursor.execute(sql1)
data = cursor.fetchall()
print('全部資料：')
print(data)

sql2 = "update score set 國文=98 where 座號 = '%s' " % ('4')  #修改資料
cursor.execute(sql2)
cursor.execute(sql1)
data = cursor.fetchall()
print('修改後資料：')
print(data)

sql3 = "delete from score where 座號 = '%s' " % ('6')  #刪除資料
cursor.execute(sql3)
cursor.execute(sql1)
data = cursor.fetchall()
print('刪除後資料：')
print(data)

conn.commit()  #提交資料庫
cursor.close()
conn.close()

```
## mysqltable.py
```
import pymysql
conn = pymysql.connect('localhost',port=3306,user='root',passwd='1234',charset='utf8', db='pythondb')  #連結資料庫

with conn.cursor() as cursor:
    sql = """
    CREATE TABLE IF NOT EXISTS Scores (
      ID int NOT NULL AUTO_INCREMENT PRIMARY KEY,
      Name varchar(20),
      Chinese int(3),
      English int(3),
      Math int(3)
    );
    """
    cursor.execute(sql)  #執行SQL指令
    conn.commit()  #提交資料庫
conn.close()
```
## mysqlupdate.py
```
import pymysql
conn = pymysql.connect('localhost',port=3306,user='root',passwd='1234',charset='utf8', db='pythondb')  #連結資料庫

with conn.cursor() as cursor:
    sql = "update scores set Chinese = 98 where ID = 4"
    cursor.execute(sql)
    conn.commit()
    sql = "select * from scores where ID = 4"
    cursor.execute(sql)    
    data = cursor.fetchone()
    print(data)
    
conn.close()
```
## sqlite_crud1.py
```
import sqlite3
conn = sqlite3.connect('test.sqlite') # 建立資料庫連線

# 建立一個資料表
sqlstr='''CREATE TABLE "contact" \
("id"  INTEGER PRIMARY KEY NOT NULL,
 "name"  TEXT NOT NULL,
 "tel"  TEXT NOT NULL)
'''
conn.execute(sqlstr)
conn.commit() # 更新
conn.close()  # 關閉資料庫連線
```
## sqlite_crud2.py
```
import sqlite3
conn = sqlite3.connect('test.sqlite') # 建立資料庫連線
# 定義資料串列
datas = [[1, 'David', '02-123456789'],
        [2, 'Lily', '02-987654321'],]
for data in datas:
    # 新增資料
    conn.execute("INSERT INTO contact (id, name, tel) VALUES \
                 ({}, '{}', '{}')".format(data[0], data[1], data[2]))
conn.commit() # 更新
conn.close()  # 關閉資料庫連線
```
## sqlite_crud3.py
```
import sqlite3
conn = sqlite3.connect('test.sqlite') # 建立資料庫連線
# 更新資料
conn.execute("UPDATE contact SET name='{}' WHERE id={}".format('Ken', 1))
conn.commit() # 更新
conn.close()  # 關閉資料庫連線
```
## sqlite_crud4.py
```
import sqlite3
conn = sqlite3.connect('test.sqlite') # 建立資料庫連線
# 刪除資料
conn.execute("DELETE FROM contact WHERE id={}".format(1))
conn.commit() # 更新
conn.close()  # 關閉資料庫連線
```
## sqlite_cursor.py
```
import sqlite3
conn = sqlite3.connect('test.sqlite') # 建立資料庫連線
cursor = conn.cursor() # 建立 cursor 物件

# 建立一個資料表
sqlstr='''CREATE TABLE IF NOT EXISTS table01 \
("id"  INTEGER PRIMARY KEY NOT NULL,
 "name"  TEXT NOT NULL,
 "tel"  TEXT NOT NULL)
'''
cursor.execute(sqlstr)

# 新增一筆記錄
sqlstr='insert into table01 values(1, "David", "02-1234567")'
cursor.execute(sqlstr)
conn.commit() # 更新
conn.close()  # 關閉資料庫連線
```
## xlsx_read.py
```
import openpyxl
#  讀取檔案
workbook = openpyxl.load_workbook('test.xlsx')
# 取得第 1 個工作表
sheet = workbook.worksheets[0]
# 取得指定儲存格
print(sheet['A1'], sheet['A1'].value)
# 取得總行、列數
print(sheet.max_row, sheet.max_column)
# 顯示 cell資料
for i in range(1, sheet.max_row+1):
    for j in range(1, sheet.max_column+1):
        print(sheet.cell(row=i, column=j).value,end="   ")
    print()
sheet['A3'] = 'Perry' 
workbook.save('test.xlsx')      
```
## xlsx_write.py
```
import openpyxl   
# 建立一個工作簿     
workbook=openpyxl.Workbook()   
# 取得第 1 個工作表
sheet = workbook.worksheets[0]
# 以儲存格位置寫入資料
sheet['A1'] = 'Hello'
sheet['B1'] = 'World'
# 以串列寫入資料
listtitle=["姓名","電話"]
sheet.append(listtitle)  
listdata=["David","0999-1234567"]
sheet.append(listdata)  
# 儲存檔案   
workbook.save('test.xlsx')
```
# ch13
---
## bar1.py
```
import matplotlib.pyplot as plt

listx = ['c','c++','c#','java','python']
listy = [45,28,38,32,50]
plt.bar(listx, listy, width=0.5, color='rgb')
plt.title("資訊程式課程選修人數")
plt.xlabel("程式課程")
plt.ylabel("選修人數")
# 設定中文字型及負號正確顯示
plt.rcParams["font.sans-serif"] = "SimHei" 
plt.rcParams["axes.unicode_minus"] = False
plt.show()
```
## bar2.py
```
import matplotlib.pyplot as plt

listy = ['c','c++','c#','java','python']
listx = [45,28,38,32,50]
plt.barh(listy, listx, height=0.5, color='rgb')
plt.title("資訊程式課程選修人數")
plt.xlabel("程式課程")
plt.ylabel("選修人數")
# 設定中文字型及負號正確顯示
plt.rcParams["font.sans-serif"] = "SimHei" 
plt.rcParams["axes.unicode_minus"] = False
plt.show()
```
## bar3.py
```
import matplotlib.pyplot as plt

listx = ['c','c++','c#','java','python']
listy1 = [25,20,20,16,28]
listy2 = [20,8,18,16,22]
plt.bar(listx, listy1, width=0.5, label='男')
plt.bar(listx, listy2, width=0.5, bottom=listy1, label='女')
plt.legend()
plt.title("資訊程式課程選修人數")
plt.xlabel("程式課程")
plt.ylabel("選修人數")
# 設定中文字型及負號正確顯示
plt.rcParams["font.sans-serif"] = "SimHei" 
plt.rcParams["axes.unicode_minus"] = False
plt.show()
```
## bar4.py
```
import matplotlib.pyplot as plt

width = 0.25
listx = ['c','c++','c#','java','python']
listx1 = [x - width/2 for x in range(len(listx))]
listx2 = [x + width/2 for x in range(len(listx))]
listy1 = [25,20,20,16,28]
listy2 = [20,8,18,16,22]
plt.bar(listx1, listy1, width, label='男')
plt.bar(listx2, listy2, width, label='女')
plt.xticks(range(len(listx)), labels=listx)
plt.legend()
plt.title("資訊程式課程選修人數")
plt.xlabel("程式課程")
plt.ylabel("選修人數")
# 設定中文字型及負號正確顯示
plt.rcParams["font.sans-serif"] = "SimHei" 
plt.rcParams["axes.unicode_minus"] = False
plt.show()
```
## figure.py
```
import matplotlib.pyplot as plt
# 新增圖表區
plt.figure()
plt.plot([1,2,3])
# 新增圖表區並設定屬性
plt.figure(figsize=[8,4], dpi=84, facecolor="whitesmoke", edgecolor="r", linewidth=1, frameon=True)
plt.plot([1,2,3])

plt.show()
```
## figure2.py
```
import matplotlib.pyplot as plt

plt.figure()
plt.plot([1,2,3])
plt.grid(axis='y')
plt.show()
```
## pie.py
```
import matplotlib.pyplot as plt

sizes = [25, 30, 15, 10]
labels = ["北部", "西部", "南部", "東部"]
colors = ["red", "green", "blue", "yellow"]
explode = (0, 0, 0.2, 0)
plt.pie(sizes, 
	explode = explode, 
	labels = labels, 
	colors = colors,
	labeldistance = 1.1, 
	autopct = "%2.1f%%", 
	pctdistance = 0.6,
	shadow = True,
	startangle = 90)
plt.show()
```
## plot1.py
```
import matplotlib.pyplot as plt

listx = [1,5,7,9,13,16]
listy = [15,50,80,40,70,50]
plt.plot(listx, listy, 'g--*', markersize=12)
plt.show()
```
## plot2.py
```
import matplotlib.pyplot as plt

listx = [1,5,7,9,13,16]
listy = [15,50,80,40,70,50]
plt.plot(listx, listy, color="red", lw="2.0", ls="--", label="label")
plt.title("Chart Title", fontsize=20)	#圖表標題
plt.xlabel("X-Label", fontsize=14)		#x座標標題
plt.ylabel("Y-Label", fontsize=14)		#y座標標題
plt.legend()
plt.show()
```
## plot3.py
```
import matplotlib.pyplot as plt

listx = [1,5,7,9,13,16]
listy = [15,50,80,40,70,50]
plt.plot(listx, listy, color="red", lw="2.0", ls="--", label="label")
plt.title("Chart Title")	#圖表標題
plt.xlabel("X-Label")		#x座標標題
plt.ylabel("Y-Label")		#y座標標題
plt.xlim(0, 20)            #設定x座標範圍
plt.ylim(0, 100)             #設定y座標範圍
plt.legend()
plt.show()
```
## plot4.py
```
import matplotlib.pyplot as plt

listx = [1,5,7,9,13,18]
listy = [15,50,80,40,70,50]
plt.plot(listx, listy, color="red", lw="2.0", ls="--", label="label")
plt.title("Chart Title")	#圖表標題
plt.xlabel("X-Label")		#x座標標題
plt.ylabel("Y-Label")		#y座標標題
plt.xlim(0, 20)            #設定x座標範圍
plt.ylim(0, 100)             #設定y座標範圍
plt.grid(color='black', linestyle=":", linewidth='1', alpha=0.5)
plt.legend()
plt.show()
```
## plot5.py
```
import matplotlib.pyplot as plt

listx1 = [1,5,7,9,13,16]
listy1 = [15,50,80,40,70,50]
plt.plot(listx1, listy1, 'r-.s')
listx2 = [2,6,8,11,14,16]
listy2 = [10,40,30,50,80,60]
plt.plot(listx2, listy2, 'y-s')
plt.show()
```
## plot5_.py
```
import matplotlib.pyplot as plt
month = [1,2,3,4,5,6,7,8,9,10,11,12]
listy1 = [128,210,199,121,105,98,152,107,150,122,180,220]
plt.plot(month, listy1, 'r-.s', lw=2, ms=10, label="Taipei")
listy2 = [150,200,180,110,100,80,80,100,130,120,110,200]
plt.plot(month, listy2, 'g--*', lw=2, ms=10, label="Taichung")
plt.legend()
plt.xticks(month)
plt.ylim(50, 250)
plt.title("Sales Report", fontsize=18)
plt.xlabel("Month", fontsize=12)
plt.ylabel("Million", fontsize=12)
plt.show()
```
## plot6.py
```
import matplotlib.pyplot as plt

listx1 = [1,5,7,9,13,16]
listy1 = [15,50,80,40,70,50]
listx2 = [2,6,8,11,14,16]
listy2 = [10,40,30,50,80,60]
plt.plot(listx1, listy1, 'r-.s', listx2, listy2, 'y-s')
plt.show()
```
## plot6_.py
```
import matplotlib.pyplot as plt

listx1 = [1,5,7,9,13,16]
listy1 = [15,50,80,40,70,50]
plt.plot(listx1, listy1, 'r-.s', lw=2, ms=10, label="Male")
listx2 = [2,6,8,11,14,16]
listy2 = [10,40,30,50,80,60]
plt.plot(listx2, listy2, 'g--*', lw=2, ms=10, label="Female")
plt.legend()
plt.xlim(0, 20)
plt.ylim(0, 100)
plt.title("費用", fontsize=18)
plt.xlabel("Age", fontsize=12)
plt.ylabel("Money", fontsize=12)
plt.tick_params(axis='y', color='red')
plt.rcParams["font.sans-serif"] = "SimHei"
plt.rcParams["axes.unicode_minus"] = False
plt.show()
```
## plot7.py
```
import matplotlib.pyplot as plt

listx = [1000,2000,3000,4000,5000]
listy = [15,50,80,70,50]
plt.plot(listx, listy)
plt.xticks(listx)
plt.tick_params(axis='both', labelsize=16, color='red')
plt.show()
```
## plot8.py
```
import matplotlib.pyplot as plt
year = [2015,2016,2017,2018,2019]
city1 = [128,150,199,180,150]
plt.plot(year, city1, 'r-.s', lw=2, ms=10, label="Taipei")
city2 = [120,145,180,170,120]
plt.plot(year, city2, 'g--*', lw=2, ms=10, label="Taichung")
plt.legend()
plt.ylim(50, 250)
plt.xticks(year)
plt.title("Sales Report", fontsize=18)
plt.xlabel("Year", fontsize=12)
plt.ylabel("Million", fontsize=12)
plt.grid(color='k', ls=':', lw=1, alpha=0.5)
plt.show()
```
## plot9.py
```
import matplotlib.pyplot as plt
year = [2015,2016,2017,2018,2019]
city1 = [128,150,199,180,150]
plt.plot(year, city1, 'r-.s', lw=2, ms=10, label="台北")
city2 = [120,145,180,170,120]
plt.plot(year, city2, 'g--*', lw=2, ms=10, label="台中")
plt.legend()
plt.ylim(50, 250)
plt.xticks(year)
plt.title("銷售報表", fontsize=18)
plt.xlabel("年度", fontsize=12)
plt.ylabel("百萬", fontsize=12)
# 設定中文字型及負號正確顯示
plt.rcParams["font.sans-serif"] = "Microsoft JhengHei" #也可設mingliu或DFKai-SB
plt.rcParams["axes.unicode_minus"] = False
plt.show()
```
## plotly1.py
```
import plotly
from plotly.graph_objs import Scatter

#plotly.offline.init_notebook_mode(connected=True)

data = [Scatter(x=["林大明", "陳聰明", "黃美麗", "熊小娟"], y=[67,89,72,95])]
plotly.offline.plot({
    "data": data
}) 
```
## subplot_1.py
```
import matplotlib.pyplot as plt

listx = [1,2,3,4,5]

listy1 = [15,50,80,40,70]
plt.subplot(2,1,1)
plt.ylim(0, 100)
plt.plot(listx, listy1, 'r-s')

listy2 = [80,20,60,50,20]
plt.subplot(2,1,2)
plt.ylim(0, 100)
plt.plot(listx, listy2, 'g--o')

plt.show()

#plt.rcParams['figure.figsize'] = [10, 10]
#plt.rcParams['figure.dpi'] = 72
#plt.rcParams.keys
```
## subplot_2.py
```
import matplotlib.pyplot as plt

listx = [1,2,3,4,5]

listy1 = [15,50,80,40,70]
plt.axes([0.1, 0, 0.8, 0.8])
plt.ylim(0, 100)
plt.plot(listx, listy1, 'r-s')

listy2 = [80,20,60,50,20]
plt.axes([1, 0, 0.8, 0.8])
plt.ylim(0, 100)
plt.plot(listx, listy2, 'g--o')

plt.axes([0.1, 1, 0.8, 0.8])
plt.ylim(0, 100)
plt.plot(listx, listy1, 'r-s')

plt.axes([1, 1, 0.8, 0.8])
plt.ylim(0, 100)
plt.plot(listx, listy2, 'g--o')

plt.show()

#plt.rcParams['figure.figsize'] = [10, 10]
#plt.rcParams['figure.dpi'] = 72
#plt.rcParams.keys
```
## subplot1.py
```
import matplotlib.pyplot as plt

plt.figure(figsize=[8,8])
plt.subplot(211)
plt.title(label='Chart 1')
plt.plot([1,2,3],'r:o')

plt.subplot(212)
plt.title(label='Chart 2')
plt.plot([1,2,3],'g--o')

plt.show()
```
## subplot2.py
```
import matplotlib.pyplot as plt

plt.figure(figsize=[8,8])
plt.subplot(121)
plt.title(label='Chart 1')
plt.plot([1,2,3],'r:o')

plt.subplot(122)
plt.title(label='Chart 2')
plt.plot([1,2,3],'g--o')

plt.show()
```
## subplot3.py
```
import matplotlib.pyplot as plt

plt.figure(figsize=[8,8])
plt.subplot(221)
plt.title(label='Chart 1')
plt.plot([1,2,3],'r:o')

plt.subplot(222)
plt.title(label='Chart 2')
plt.plot([1,2,3],'g--o')

plt.subplot(223)
plt.title(label='Chart 3')
plt.plot([1,2,3],'b:o')

plt.subplot(224)
plt.title(label='Chart 4')
plt.plot([1,2,3],'y--o')

plt.show()
```
## subplot4.py
```
import matplotlib.pyplot as plt

plt.figure(figsize=[8,4])
plt.axes([0,0,0.4,1])
plt.title(label='Chart 1')
plt.plot([1,2,3],'r:o')

plt.axes([0.5,0,0.4,1])
plt.title(label='Chart 2')
plt.plot([1,2,3],'g--o')

plt.show()
```
## subplot5.py
```
import matplotlib.pyplot as plt

plt.figure(figsize=[8,4])
plt.axes([0,0,0.8,1])
plt.title(label='Chart 1')
plt.plot([1,2,3],'r:o')

plt.axes([0.55,0.1,0.2,0.2])
plt.title(label='Chart 2')
plt.plot([1,2,3],'g--o')

plt.show()
```
## twstock1.py
```
import twstock
# 以鴻海的股票代號建立 Stock 物件
stock = twstock.Stock('2317')  
print(stock.price)
```
## twstock2.py
```
import twstock
# 以鴻海的股票代號建立 Stock 物件
stock = twstock.Stock('2317')  
print("日期：",stock.date[-1])
print("開盤價：",stock.open[-1])
print("最高價：",stock.high[-1])
print("最低價：",stock.low[-1])
print("收盤價：",stock.price[-1])
```
## twstock3.py
```
import twstock
# 以鴻海的股票代號建立 Stock 物件
stock = twstock.Stock('2317')  
# 取得 2019 年 12 月的資料
stocklist = stock.fetch(2019,12)   
for s in stocklist:
    print(s.date.strftime('%Y-%m-%d'), end='\t')
    print(s.open, end='\t')
    print(s.high, end='\t')
    print(s.low, end='\t')
    print(s.close)
```
## twstock4.py
```
import twstock
# 鴻海股票即時交易資訊
real = twstock.realtime.get('2317') 
if real['success']:  #如果讀取成功
    print('即時股票資料：',real['info']['name'])     
    print('開盤價：',real['realtime']['open'], end=', ')
    print('最高價：',real['realtime']['high'], end=', ')  
    print('最低價：',real['realtime']['low'], end=', ')
    print('目前股價：',real['realtime']['latest_trade_price'])   
else:
    print('錯誤：' + real['rtmessage'])  

```
## twstock5.py
```
import matplotlib.pyplot as plt
import twstock
# 以鴻海的股票代號建立 Stock 物件
stock = twstock.Stock('2317')  
# 取得 2019 年 12 月的資料
stocklist = stock.fetch(2019,12)   
listx = []
listy = []
for s in stocklist:
    listx.append(s.date.strftime('%Y-%m-%d'))
    listy.append(s.close)

plt.figure(figsize=[10,5])
plt.title('鴻海2019年12月股價',fontsize=18)
plt.xlabel("日期",fontsize=14)
plt.ylabel("股價",fontsize=14)
plt.plot(listx, listy, 'r:s')
plt.xticks(rotation=45)
plt.grid('k:', alpha=0.5)
plt.ylim(88,93)
plt.yticks([88,89,90,91,92,93])
plt.rcParams["font.sans-serif"] = "SimHei" 
plt.rcParams["axes.unicode_minus"] = False

plt.show() 
```
## twstock6.py
```
import matplotlib.pyplot as plt
import twstock
companys = ['2330','2912','3293']
plt.figure(figsize=[10,5])
for company in companys:
    stock = twstock.Stock(company)  
    # 取得 2019 年 12 月的資料
    stocklist = stock.fetch(2019,12)   
    listx = []
    listy = []
    for s in stocklist:
        listx.append(s.date.strftime('%Y-%m-%d'))
        listy.append(s.close)
    
    plt.plot(listx, listy)
    plt.xticks(rotation=45)
plt.show() 
```
## twstock7.py
```
import matplotlib.pyplot as plt
import twstock
import time
#plt.figure(figsize=[12,30])
stock = twstock.Stock('2317') 
slist = []
for i in range(1,13):
    stocklist = stock.fetch(2019,i)
    [slist.append(s) for s in stocklist]
#    listx = [s.date.strftime('%d') for s in stocklist]
#    listy = [s.close for s in stocklist]
#    plt.subplot('62{}'.format(i))
#    plt.xticks(rotation=45)
#    plt.title(label="{}月".format(i))
#    plt.rcParams["font.sans-serif"] = "SimHei" 
#    plt.rcParams["axes.unicode_minus"] = False
#    plt.plot(listx, listy)
    print(len(slist))
    time.sleep(5)
    if i == 6:
        time.sleep(20)
    

#plt.show()

#lista = []
#list1 = [1,2,3,4,5]
#list2 = [7,8,9,10,11]
#list1.append(list2)
#list1
#%%
import csv
with open('2019_2330.csv', 'w', newline='') as f:
    writer = csv.writer(f)
    writer.writerows(slist)
#%%
import matplotlib.pyplot as plt
import csv
with open('2019_2330.csv', 'r', newline='') as f:
    datas = csv.reader(f)  
    listx = []
    listy = []
    for data in datas:
        listx.append(data[0])
        listy.append(data[5])

#    print(len(datas))
#    print(len(listx), len(listy))
    plt.figure(figsize=(20,5))
    plt.plot(listx, listy)
    plt.yticks(range(10,200,10))
    plt.show() 
#    print([x[6] for x in datas])

#    print(type(datas))
#%%
plt.figure(figsize=(20,5))
plt.plot([x.close for x in slist])
plt.show() 

#%%
for data in datas:
    print(data)
    
#%%
lsit1=[1,2,3,4]    
list1[0]
```
# ch14
---
## df1.py
```
import pandas as pd
df = pd.DataFrame([[65,92,78,83,70], 
                   [90,72,76,93,56], 
                   [81,85,91,89,77], 
                   [79,53,47,94,80]])
print(df)
```
## df2.py
```
import pandas as pd
df = pd.DataFrame([[65,92,78,83,70], 
                   [90,72,76,93,56], 
                   [81,85,91,89,77], 
                   [79,53,47,94,80]],
                   index=['王小明','李小美','陳大同','林小玉'],
                   columns=['國文','英文','數學','自然','社會'])
print(df)
```
## df3.py
```
import pandas as pd
scores = {'國文':{'王小明':65,'李小美':90,'陳大同':81,'林小玉':79},
          '英文':{'王小明':92,'李小美':72,'陳大同':85,'林小玉':53},
          '數學':{'王小明':78,'李小美':76,'陳大同':91,'林小玉':47},
          '自然':{'王小明':83,'李小美':93,'陳大同':89,'林小玉':94},
          '社會':{'王小明':70,'李小美':56,'陳大同':94,'林小玉':80}}
df = pd.DataFrame(scores)
print(df)    
```
## df3_.py
```
import pandas as pd
scores = {'王小明':{'國文':65,'英文':92,'數學':78,'社會':83,'自然':70},
          '李小美':{'國文':90,'英文':72,'數學':76,'社會':93,'自然':56},
          '陳大同':{'國文':81,'英文':85,'數學':91,'社會':89,'自然':77},
          '林小玉':{'國文':79,'英文':53,'數學':47,'社會':94,'自然':80}}
df = pd.DataFrame(scores)
print(df)    
```
## df4.py
```
import pandas as pd
se1 = pd.Series({'王小明':65,'李小美':90,'陳大同':81,'林小玉':79})
se2 = pd.Series({'王小明':92,'李小美':72,'陳大同':85,'林小玉':53})
se3 = pd.Series({'王小明':78,'李小美':76,'陳大同':91,'林小玉':47})
se4 = pd.Series({'王小明':83,'李小美':93,'陳大同':89,'林小玉':94})
se5 = pd.Series({'王小明':70,'李小美':56,'陳大同':94,'林小玉':80})
df = pd.DataFrame({'國文':se1, '英文':se2, '數學':se3, '自然':se4, '社會':se5})
print(df)
```
## df5.py
```
import pandas as pd
se1 = pd.Series({'王小明':65,'李小美':90,'陳大同':81,'林小玉':79})
se2 = pd.Series({'王小明':92,'李小美':72,'陳大同':85,'林小玉':53})
se3 = pd.Series({'王小明':78,'李小美':76,'陳大同':91,'林小玉':47})
se4 = pd.Series({'王小明':83,'李小美':93,'陳大同':89,'林小玉':94})
se5 = pd.Series({'王小明':70,'李小美':56,'陳大同':94,'林小玉':80})
df = pd.concat([se1,se2,se3,se4,se5], axis=0)
df.columns=['國文','英文','數學','自然','社會']
print(df)
```
## df6.py
```
import pandas as pd
scores = {'國文':{'王小明':65,'李小美':90,'陳大同':81,'林小玉':79},
          '英文':{'王小明':92,'李小美':72,'陳大同':85,'林小玉':53},
          '數學':{'王小明':78,'李小美':76,'陳大同':91,'林小玉':47},
          '自然':{'王小明':83,'李小美':93,'陳大同':89,'林小玉':94},
          '社會':{'王小明':70,'李小美':56,'陳大同':94,'林小玉':80}}
df = pd.DataFrame(scores)
print(df["自然"])
print(df[["國文", "數學", "自然"]])
print(df[df["國文"] >= 80])
print(df.values)
print(df.values[1])
print(df.values[1][2])
# loc
print(df.loc["林小玉", "社會"])
print(df.loc["王小明", ["國文","社會"]])
print(df.loc[["王小明", "李小美"], ["數學", "自然"]])
print(df.loc["王小明":"陳大同", "數學":"社會"])
print(df.loc["陳大同", :])
print(df.loc[:"李小美", "數學":"社會"])
print(df.loc["李小美":, "數學":"社會"])
print(df.iloc[3, 4])
# iloc
df.iloc[0, [0, 4]]
df.iloc[[0, 1], [2, 3]]
df.iloc[0:3, 2:5]
df.iloc[2, :]
df.iloc[:2, 2:5]
df.iloc[1:, 2:5]
# head() tail()
df.head(2)
df.tail(2)
```
## df7.py
```
import pandas as pd
scores = {'國文':{'王小明':65,'李小美':90,'陳大同':81,'林小玉':79},
          '英文':{'王小明':92,'李小美':72,'陳大同':85,'林小玉':53},
          '數學':{'王小明':78,'李小美':76,'陳大同':91,'林小玉':47},
          '自然':{'王小明':83,'李小美':93,'陳大同':89,'林小玉':94},
          '社會':{'王小明':70,'李小美':56,'陳大同':94,'林小玉':80}}
df = pd.DataFrame(scores)
# 排序
print(df.sort_values(by="數學", ascending=False))
print(df.sort_index(axis=0))
# 修改
df1 = df.loc["王小明"]["數學"] = 90
print(df)
df2 = df.loc["王小明", :] = 80
print(df)
# 刪除
df.drop("王小明")
df.drop("數學", axis=1)
df.drop(["數學", "自然"], axis=1)
df.drop(df.index[1:4])
df.drop(df.columns[1:4], axis=1)
```
## np1.py
```
import numpy as np
np1 = np.array([1,2,3,4])	#使用list
np2 = np.array((5,6,7,8))	#使用tuple
print(np1)
print(np2)
print(type(np1), type(np2))
```
## np2.py
```
import numpy as np
na = np.array([1,2,3,4], dtype=int)
print(na)
na = np.array([1,2,3,4], dtype=float)
print(na)
```
## np3.py
```
import numpy as np
na = np.arange(0, 31, 2)
print(na)
```
## np4.py
```
import numpy as np
na = np.linspace(1, 15, 3)
print(na)
```
## np5.py
```
import numpy as np
a = np.zeros((5,))
print(a)
```
## np6.py
```
import numpy as np
b = np.ones((5,))
print(b)
```
## np7.py
```
import numpy as np
c = np.empty((5,))
print(c)
```
## np8.py
```
import numpy as np
listdata = [[1,2,3,4,5],
            [6,7,8,9,10],
            [11,12,13,14,15]]
na = np.array(listdata)
print(na)
print('維度', na.ndim)
print('形狀', na.shape)
print('數量', na.size)
```
## np9.py
```
import numpy as np
adata = np.arange(1,17)
print(adata)
bdata = adata.reshape(4,4)
print(bdata)
```
## np10.py
```
import numpy as np
na = np.arange(0,6)
print(na)           #[0 1 2 3 4 5]
print(na[0])        #0
print(na[5])        #5
print(na[1:5])      #[1 2 3 4]
print(na[1:5:2])    #[1 3]
print(na[5:1:-1])   #[5 4 3 2]
print(na[:])        #[0 1 2 3 4 5]
print(na[:3])       #[0 1 2]
print(na[3:])       #[3 4 5]
```
## np11.py
```
import numpy as np
na = np.arange(1, 17).reshape(4, 4)
print(na[2, 3])			#12
print(na[1, 1:3])		#[6,7]
print(na[1:3, 2])		#[7,11]
print(na[1:3, 1:3])		#[[6,7],[7,11]]
print(na[::2, ::2])		#[[1,3],[9,11]]
print(na[:, 2])			#[3,7,11,15]
print(na[1, :])			#[5,6,7,8]
print(na[:, :])			#矩陣全部
```
## np12.py
```
import numpy as np
print('1.產生2x3 0~1之間的隨機浮點數\n',
      np.random.rand(2,3))
print('2.產生2x3常態分佈的隨機浮點數\n',
      np.random.randn(2,3))
print('3.產生0~4(不含5)隨機整數\n',
      np.random.randint(5))
print('4.產生2~4(不含5)5個隨機整數\n',
      np.random.randint(2,5,[5]))
print('5.產生3個 0~1之間的隨機浮點數\n',
      np.random.random(3),'\n',
      np.random.random_sample(3),'\n',
      np.random.sample(3))
print('6.產生0~4(不含5)2x3的隨機整數\n',
      np.random.choice(5,[2,3]))
print('7.產生0~42(不含43)6個不重複的隨機整數\n',
      np.random.choice(43,6,replace=False))
```
## np13.py
```
import numpy as np
a = np.genfromtxt('scores.csv', delimiter=',', skip_header=1)
print(a.shape)
```
## np14.py
```
import numpy as np
a = np.arange(1,10).reshape(3,3)
b = np.arange(10,19).reshape(3,3)
print('a 陣列內容：\n', a)
print('b 陣列內容：\n', b)
print('a 陣列元素都加值：\n', a + 1)
print('a 陣列元素都平方：\n', a ** 2)
print('a 陣列元素加判斷：\n', a < 5)
print('a 陣列取出第一個row都加1：\n', a[0,:] + 1)
print('a 陣列取出第一個col都加1：\n', a[:,0] + 1)
print('a b 陣列對應元素相加：\n', a + b)
print('a b 陣列對應元素相乘：\n', a * b)
print('a b 陣列點積計算：\n', np.dot(a,b))
```
## np15.py
```
import numpy as np
a = np.arange(1,10).reshape(3,3)
print('陣列的內容：\n', a)
print('1.最小值與最大值：\n',
      np.min(a), np.max(a))
print('2.每一直行最小值與最大值：\n',
      np.min(a, axis=0), np.max(a, axis=0))
print('3.每一橫列最小值與最大值：\n',
      np.min(a, axis=1), np.max(a, axis=1))
print('4.加總、乘積及平均值：\n',
      np.sum(a), np.prod(a), np.mean(a))
print('5.每一直行加總、乘積與平均值：\n',
      np.sum(a, axis=0), np.prod(a, axis=0), np.mean(a, axis=0))
print('6.每一橫列加總、乘積與平均值：\n',
      np.sum(a, axis=1), np.prod(a, axis=1), np.mean(a, axis=1))
```
## np15_.py
```
import numpy as np
na = np.genfromtxt('scores.csv', delimiter=',', skip_header=1)
print('國文最高分數：', na[:,1].max())
print('英文最低分數：', na[:,2].min())
print('數學平均分數：', na[:,3].mean())
total1 = na[:,1] + na[:,2] + na[:,3]
print(total1)
print('全班最高總分：',total1.max())

total2 = na[:,1:4].sum(axis=1)
print(total2)
print('全班最高總分：',total2.max())
```
## np16.py
```
import numpy as np
a = np.random.randint(100,size=50)
print('陣列的內容：', a)
print('1.標準差：', np.std(a))
print('2.變異數：', np.var(a))
print('3.中位數：', np.median(a))
print('4.百分比值：', np.percentile(a, 80))
print('5.最大最小差值：', np.ptp(a))
```
## np17.py
```
import numpy as np
a = np.random.choice(50, size=10, replace=False)
print('排序前的陣列：', a)
print('排序後的陣列：', np.sort(a))
print('排序後的索引：', np.argsort(a))
#用索引到陣列取值
for i in np.argsort(a):
    print(a[i], end=',')
```
## np18.py
```
import numpy as np
a = np.random.randint(0,10,(3,5))
print('原陣列內容：')
print(a)
print('將每一直行進行排序：')
print(np.sort(a, axis=0))
print('將每一橫列進行排序：')
print(np.sort(a, axis=1))
```
## pd1.py
```
import pandas as pd
df = pd.Series(['a','b','c','d','e'])
print(se[1:3])
```
## plot1.py
```
import pandas as pd
import matplotlib.pyplot as plt
# 設定中文字型及負號正確顯示
plt.rcParams["font.sans-serif"] = "Microsoft JhengHei" #也可設mingliu或DFKai-SB

plt.rcParams["axes.unicode_minus"] = False 

df = pd.DataFrame([[250,320,300,312,280],
                   [280,300,280,290,310],
                   [220,280,250,305,250]],
                   index=['北部','中部','南部'],
                   columns=[2015,2016,2017,2018,2019])
g1 = df.plot(kind='bar', title='長條圖', figsize=[10,5])
g2 = df.plot(kind='barh', title='橫條圖', figsize=[10,5])
g3 = df.plot(kind='bar', stacked=True, title='堆疊圖', figsize=[10,5])
```
## plot2.py
```
import pandas as pd
import matplotlib.pyplot as plt
# 設定中文字型及負號正確顯示
plt.rcParams["font.sans-serif"] = "Microsoft JhengHei" #也可設mingliu或DFKai-SB
plt.rcParams["axes.unicode_minus"] = False 

df = pd.DataFrame([[250,320,300,312,280],
                   [280,300,280,290,310],
                   [220,280,250,305,250]],
                   index=['北部','中部','南部'],
                   columns=[2015,2016,2017,2018,2019])
g1 = df.iloc[0].plot(kind='line', legend=True, xticks=range(2015,2020), title='公司分區年度銷售表', figsize=[10,5])
g1 = df.iloc[1].plot(kind='line', legend=True, xticks=range(2015,2020))
g1 = df.iloc[2].plot(kind='line', legend=True, xticks=range(2015,2020))
```
## plot3.py
```
import pandas as pd
import matplotlib.pyplot as plt
# 設定中文字型及負號正確顯示
plt.rcParams["font.sans-serif"] = "Microsoft JhengHei"  #也可設mingliu或DFKai-SB
plt.rcParams["axes.unicode_minus"] = False 

df = pd.DataFrame([[250,320,300,312,280],
                   [280,300,280,290,310],
                   [220,280,250,305,250]],
                   index=['北部','中部','南部'],
                   columns=[2015,2016,2017,2018,2019])
df.plot(kind='pie', subplots=True, figsize=[20,20])
```
## read_cvs.py
```
import pandas as pd
data = pd.read_csv("scores2.csv", header=0, index_col=0)
print(data)
print(type(data))
```
## read_html.py
```
import pandas as pd
url = 'https://www.tiobe.com/tiobe-index/'
tables = pd.read_html(url, header=0, keep_default_na=False)
print(tables[0])
```
## se1.py
```
import pandas as pd
se = pd.Series([1,2,3,4,5])
print(se)           #顯示Series
print(se.values)    #顯示值
print(se.index)     #顯示索引
```
## se2.py
```
import pandas as pd
se = pd.Series([1,2,3,4,5])
print(se[2])
print(se[2:5])
```
## se3.py
```
import pandas as pd
se = pd.Series([1,2,3,4,5], index=['a','b','c','d','e'])
print(se)
print(se['b'])
print(se['c':'d'])
```
## se4.py
```
import pandas as pd
dict1 = {'Taipei': '台北', 'Taichung': '台中', 'Kaohsiung': '高雄'}
se = pd.Series(dict1)
print(se)           #顯示Series
print(se.values)    #顯示值
print(se.index)     #顯示索引
print(se['Taipei']) #用索引取值
print(se['Taichung':'Kaohsiung'])
```
## to_cvs.py
```
import pandas as pd
scores = {'國文':{'王小明':65,'李小美':90,'陳大同':81,'林小玉':79},
          '英文':{'王小明':92,'李小美':72,'陳大同':85,'林小玉':53},
          '數學':{'王小明':78,'李小美':76,'陳大同':91,'林小玉':47},
          '自然':{'王小明':83,'李小美':93,'陳大同':89,'林小玉':94},
          '社會':{'王小明':70,'李小美':56,'陳大同':94,'林小玉':80}}
df = pd.DataFrame(scores)
df.to_csv('scores3.csv', encoding='utf-8-sig')
```
# ch15
---
## get1.py
```
from flask import Flask
from flask import request
app = Flask(__name__)

from flask import render_template
@app.route('/get1', methods=['GET'])
def get1():
    name = request.args.get('name')
    city = request.args.get('city')
    return render_template('get1.html', **locals())

if __name__ == '__main__':
    app.run()

```
## hello.py
```
from flask import Flask
app = Flask(__name__)

@app.route('/hello')
def hello():
    return '歡迎來到 Flask!'

if __name__ == '__main__':
    app.run()

```
## hello2.py
```
from flask import Flask
app = Flask(__name__)

@app.route('/hello/<name>')
def hello(name):
    return '{}，歡迎來到 Flask!'.format(name)

if __name__ == '__main__':
    app.run()

```
## index.py
```
from flask import Flask
app = Flask(__name__)

@app.route('/')
@app.route('/index')
def index():
    return '這是本網站首頁!'

if __name__ == '__main__':
    app.run()

```
## post1.py
```
from flask import Flask
from flask import request
app = Flask(__name__)

from flask import render_template
@app.route('/post1')
def post1():
    return render_template('post1.html')

@app.route('/submit', methods=['POST'])
def submit():
    username = request.values['username']
    password = request.values['password']
    if username=='david' and password=='1234':
        return '歡迎光臨本網站！'
    else:
        return '帳號或密碼錯誤！'

if __name__ == '__main__':
    app.run()

```
## show.py
```
from flask import Flask
app = Flask(__name__)

from flask import render_template
@app.route('/show')
def show():
    person1={"name":"Amy","phone":"049-1234567","age":20}
    person2={"name":"Jack","phone":"02-4455666","age":25}
    person3={"name":"Nacy","phone":"04-9876543","age":17}
    persons=[person1,person2,person3]
    return render_template('show.html', **locals())

if __name__ == '__main__':
    app.run()

```
## template1.py
```
from flask import Flask
app = Flask(__name__)

from flask import render_template
@app.route('/hello')
def hello():
    return render_template('hello.html')

if __name__ == '__main__':
    app.run()

```
## template2.py
```
from flask import Flask
app = Flask(__name__)

from flask import render_template
from datetime import datetime
@app.route('/hello/<string:name>')
def hello(name):
    now = datetime.now()
    return render_template('hello2.html', **locals())

if __name__ == '__main__':
    app.run()

```
## template3.py
```
from flask import Flask
app = Flask(__name__)

from flask import render_template
from datetime import datetime
@app.route('/hello/<string:name>')
def hello(name):
    now = datetime.now()
    return render_template('hello3.html', **locals())

if __name__ == '__main__':
    app.run()

```
## test.py
```
from flask import Flask
app = Flask(__name__)

@app.route('/')
@app.route('/index')
def index():
    return '這是本網站首頁!'

if __name__ == '__main__':
    app.run()

```
## variable.py
```
from flask import Flask
app = Flask(__name__)

from flask import render_template
@app.route('/variable')
def variable():
    student = {'學號':'874523', '姓名':'張三', '性別':'男'}
    fruit = ['蘋果', '香蕉', '芭樂', '百香果']
    return render_template('variable.html', **locals())

if __name__ == '__main__':
    app.run()

```

































