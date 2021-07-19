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







































