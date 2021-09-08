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
# ch16
---
## combobox.py
```
from tkinter import *
from tkinter.ttk import *

def selected(event):
    labelVar.set(cbVar.get())

win = Tk()
win.title('最喜歡的運動')
win.geometry('300x160')

cbVar = StringVar()
cb = Combobox(win, textvariable=cbVar)
cb['value'] = ("籃球","排球","足球","其他")  #設定選項
cb.current(0)  #預設第一個選項
cb.bind('<<ComboboxSelected>>', selected)  #設定選取選項後執行的程式
cb.place(x=70, y=15)

labelVar = StringVar()  
labelShow = Label(win, textvariable=labelVar)
labelVar.set(cbVar.get())
labelShow.place(x=80, y=120)

win.mainloop()


```
## index.py
```
from tkinter import *
import requests

def showWeather(event):  #下拉選單選取選項後執行的程式
    city = cbVar.get()  #使用者選取的選項
    if city != '請選擇：':  #選擇縣市
        report = requests.get('https://weathflask.herokuapp.com/weather/' + city).text  #取得Web API資料
        jsondata = eval(report)  #轉換為字典
        showdata = city + ' 天氣資料：\n'
        showdata += '天氣狀況：' + jsondata['天氣狀況'] + '\n'
        showdata += '最高溫：' + jsondata['最高溫'] + '\n'
        showdata += '最低溫：' + jsondata['最低溫'] + '\n'
        showdata += '舒適度：' + jsondata['舒適度'] + '\n'
        showdata += '降雨機率：' + jsondata['降雨機率'] + '\n'
        labelVar.set(showdata)
    else:
        labelVar.set('請選擇縣市！')

win = Tk()
win.title('縣市天氣資料')
win.geometry('300x350')

cbVar = StringVar()
cb = Combobox(win, textvariable=cbVar)  #下拉選單元件
cb['value'] = ("請選擇：","臺北","新北","桃園","臺中","臺南","高雄","基隆","新竹","嘉義","苗栗","彰化","南投","雲林","嘉義","屏東","宜蘭","花蓮","臺東","澎湖","金門","連江" )  #設定選項
cb.current(0)  #預設第一個選項
cb.bind('<<ComboboxSelected>>', showWeather)  #設定選取選項後執行的程式
cb.place(x=70, y=15)

labelVar = StringVar()  
labelShow = Label(win, foreground='red', justify='left', textvariable=labelVar)  #標籤元件
labelVar.set('尚未選擇縣市！')
labelShow.place(x=80, y=220)

win.mainloop()
```
## weather.py
```
from flask import Flask
app = Flask(__name__)

import requests
try:
    import xml.etree.cElementTree as et
except ImportError:
    import xml.etree.ElementTree as et
@app.route('/weather/<city>')
def weather(city):
    user_key = "氣象局授權碼"
    doc_name = "F-C0032-001"
    
    cities = ["臺北","新北","桃園","臺中","臺南","高雄","基隆","新竹","嘉義"]  #市
    counties = ["苗栗","彰化","南投","雲林","屏東","宜蘭","花蓮","臺東","澎湖","金門","連江"]  #縣
    
    showdata = ''
    flagcity = False  #檢查是否為縣市名稱
    city = city.replace('台', '臺')  #氣象局資料使用「臺」
    if city in cities:  #加上「市」
        city += '市'
        flagcity = True
    elif city in counties:  #加上「縣」
        city += '縣'
        flagcity = True
    if flagcity:  #是縣市名稱
        #由氣象局API取得氣象資料
        api_link = "http://opendata.cwb.gov.tw/opendataapi?dataid=%s&authorizationkey=%s" % (doc_name,user_key)
        report = requests.get(api_link).text
        xml_namespace = "{urn:cwb:gov:tw:cwbcommon:0.1}"
        root = et.fromstring(report)
        dataset = root.find(xml_namespace + 'dataset')
        locations_info = dataset.findall(xml_namespace + 'location')
        target_idx = -1
        # 取得 <location> Elements,每個 location 就表示一個縣市資料
        for idx,ele in enumerate(locations_info):
            locationName = ele[0].text # 取得縣市名
            if locationName == city:
                target_idx = idx
                break  
        # 挑選出目前想要 location 的氣象資料
        tlist = ['天氣狀況', '最高溫', '最低溫', '舒適度', '降雨機率']
        showdata = '{'
        for i in range(len(tlist)):
            element = locations_info[target_idx][i+1] # 取出 Wx (氣象描述)
            timeblock = element[1] # 取出目前時間點的資料
            data = timeblock[2][0].text
            showdata = showdata + '"' + tlist[i] + '":"' + data + '", '
        showdata = showdata[:-2] + "}" #移除最後一個換行
    else:
        showdata = '縣市名稱不存在！'
    return showdata

if __name__ == '__main__':
    app.run()

```
## weatherapp.py
```
from tkinter import *
import requests

def showWeather(event):  #下拉選單選取選項後執行的程式
    city = cbVar.get()  #使用者選取的選項
    if city != '請選擇：':  #選擇縣市
        report = requests.get('https://weathflask.herokuapp.com/weather/' + city).text  #取得Web API資料
        jsondata = eval(report)  #轉換為字典
        showdata = city + ' 天氣資料：\n'
        showdata += '天氣狀況：' + jsondata['天氣狀況'] + '\n'
        showdata += '最高溫：' + jsondata['最高溫'] + '\n'
        showdata += '最低溫：' + jsondata['最低溫'] + '\n'
        showdata += '舒適度：' + jsondata['舒適度'] + '\n'
        showdata += '降雨機率：' + jsondata['降雨機率'] + '\n'
        labelVar.set(showdata)
    else:
        labelVar.set('請選擇縣市！')

win = Tk()
win.title('縣市天氣資料')
win.geometry('300x350')

cbVar = StringVar()
cb = Combobox(win, textvariable=cbVar)  #下拉選單元件
cb['value'] = ("請選擇：","臺北","新北","桃園","臺中","臺南","高雄","基隆","新竹","嘉義","苗栗","彰化","南投","雲林","嘉義","屏東","宜蘭","花蓮","臺東","澎湖","金門","連江" )  #設定選項
cb.current(0)  #預設第一個選項
cb.bind('<<ComboboxSelected>>', showWeather)  #設定選取選項後執行的程式
cb.place(x=70, y=15)

labelVar = StringVar()  
labelShow = Label(win, foreground='red', justify='left', textvariable=labelVar)  #標籤元件
labelVar.set('尚未選擇縣市！')
labelShow.place(x=80, y=220)

win.mainloop()
```
## weatherdata.py
```
import requests
try:
    import xml.etree.cElementTree as et
except ImportError:
    import xml.etree.ElementTree as et

user_key = "氣象局授權碼"
doc_name = "F-C0032-001"

api_link = "http://opendata.cwb.gov.tw/opendataapi?dataid=%s&authorizationkey=%s" % (doc_name,user_key)
report = requests.get(api_link).text
#print(report)
xml_namespace = "{urn:cwb:gov:tw:cwbcommon:0.1}"
root = et.fromstring(report)
dataset = root.find(xml_namespace + 'dataset')
locations_info = dataset.findall(xml_namespace + 'location')
# 取得 <location> Elements,每個 location 就表示一個縣市資料
location = '高雄市'
target_idx = -1
for idx,ele in enumerate(locations_info):
    locationName = ele[0].text # 取得縣市名
    if locationName == location:  #找到要查詢的縣市
        target_idx = idx
        break
if target_idx != -1:
    show = ''
    tlist = ['天氣狀況', '最高溫', '最低溫', '舒適度', '降雨機率']
    for i in range(5):
        element = locations_info[target_idx][i+1]  #取得weatherElement
        timeblock = element[1] # 取出目前時間點的資料
        data = timeblock[2][0].text
        show = show + tlist[i] + '：' + data + '\n'
    print(show)
else:
    print('無此縣市資料！')
    
```
# ch17
---
## firstproject
---
### __pycache__
---
### __init__.py
---
### settings.py
```
"""
Django settings for firstproject project.

Generated by 'django-admin startproject' using Django 2.2.6.

For more information on this file, see
https://docs.djangoproject.com/en/2.2/topics/settings/

For the full list of settings and their values, see
https://docs.djangoproject.com/en/2.2/ref/settings/
"""

import os

# Build paths inside the project like this: os.path.join(BASE_DIR, ...)
BASE_DIR = os.path.dirname(os.path.dirname(os.path.abspath(__file__)))


# Quick-start development settings - unsuitable for production
# See https://docs.djangoproject.com/en/2.2/howto/deployment/checklist/

# SECURITY WARNING: keep the secret key used in production secret!
SECRET_KEY = 'z1--vtq5kzp*flo)9&%o&j158q9cej6nu=ewixybr+t!ppmqqd'

# SECURITY WARNING: don't run with debug turned on in production!
DEBUG = True

ALLOWED_HOSTS = []


# Application definition

INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'myapp', # 新增的 app
]

MIDDLEWARE = [
    'django.middleware.security.SecurityMiddleware',
    'django.contrib.sessions.middleware.SessionMiddleware',
    'django.middleware.common.CommonMiddleware',
    'django.middleware.csrf.CsrfViewMiddleware',
    'django.contrib.auth.middleware.AuthenticationMiddleware',
    'django.contrib.messages.middleware.MessageMiddleware',
    'django.middleware.clickjacking.XFrameOptionsMiddleware',
]

ROOT_URLCONF = 'firstproject.urls'

TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [os.path.join(BASE_DIR, 'templates')], # 加上templates路徑
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.debug',
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]

WSGI_APPLICATION = 'firstproject.wsgi.application'


# Database
# https://docs.djangoproject.com/en/2.2/ref/settings/#databases

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': os.path.join(BASE_DIR, 'db.sqlite3'),
    }
}


# Password validation
# https://docs.djangoproject.com/en/2.2/ref/settings/#auth-password-validators

AUTH_PASSWORD_VALIDATORS = [
    {
        'NAME': 'django.contrib.auth.password_validation.UserAttributeSimilarityValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.MinimumLengthValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.CommonPasswordValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.NumericPasswordValidator',
    },
]


# Internationalization
# https://docs.djangoproject.com/en/2.2/topics/i18n/

LANGUAGE_CODE = 'zh-hant'

TIME_ZONE = 'Asia/Taipei'

USE_I18N = True

USE_L10N = True

USE_TZ = True


# Static files (CSS, JavaScript, Images)
# https://docs.djangoproject.com/en/2.2/howto/static-files/

STATIC_URL = '/static/'
STATICFILES_DIRS = [    # 加入 static 路徑
	os.path.join(BASE_DIR, 'static'),
]

```
### urls.py
```
"""firstproject URL Configuration

The `urlpatterns` list routes URLs to views. For more information please see:
    https://docs.djangoproject.com/en/2.2/topics/http/urls/
Examples:
Function views
    1. Add an import:  from my_app import views
    2. Add a URL to urlpatterns:  path('', views.home, name='home')
Class-based views
    1. Add an import:  from other_app.views import Home
    2. Add a URL to urlpatterns:  path('', Home.as_view(), name='home')
Including another URLconf
    1. Import the include() function: from django.urls import include, path
    2. Add a URL to urlpatterns:  path('blog/', include('blog.urls'))
"""
from django.contrib import admin
from django.urls import path
from myapp.views import sayhello,hello2,hello3,hello4,dice,show,djget,djpost

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', sayhello),
    path('hello2/<str:username>', hello2), 
    path('hello3/<str:username>', hello3), 
    path('hello4/<str:username>', hello4),	
    path('dice', dice),	
    path('show', show),	
    path('djget', djget),	
    path('djpost', djpost),	
]

```
### wsgi.py
```
"""
WSGI config for firstproject project.

It exposes the WSGI callable as a module-level variable named ``application``.

For more information on this file, see
https://docs.djangoproject.com/en/2.2/howto/deployment/wsgi/
"""

import os

from django.core.wsgi import get_wsgi_application

os.environ.setdefault('DJANGO_SETTINGS_MODULE', 'firstproject.settings')

application = get_wsgi_application()

```
---
## myapp
---
### __pycache__
---
### migrations
```
__pycache__
 __init__.py
```
### __init__.py
---
### admin.py
```
from django.contrib import admin

# Register your models here.

```
### apps.py
```
from django.apps import AppConfig


class MyappConfig(AppConfig):
    name = 'myapp'

```
### models.py
```
from django.db import models

# Create your models here.

```
### tests.py
```
from django.test import TestCase

# Create your tests here.

```
### views.py
```
from django.shortcuts import render
from django.http import HttpResponse
from datetime import datetime
import random  # 加入 random 套件


# Create your views here.

def sayhello(request):
    return HttpResponse("Hello Django!")

def hello2(request,username):
    return HttpResponse("Hello " + username)
   
def hello3(request,username):
    now=datetime.now()
    return render(request,"hello3.html",locals())
   
def hello4(request,username):
    now=datetime.now()
    return render(request,"hello4.html",locals())
   
def dice(request):
    no1=random.randint(1,6)   # 1~6
    no2=random.randint(1,6)   # 1~6
    no3=random.randint(1,6)   # 1~6
    # 使用 locals()傳遞所有的區域變數 
    return render(request,"dice.html",locals())   

def show(request):
    person1={"name":"Amy","phone":"049-1234567","age":20}
    person2={"name":"Jack","phone":"02-4455666","age":25}
    person3={"name":"Nacy","phone":"04-9876543","age":17}
    persons=[person1,person2,person3]
    return render(request,"show.html",locals())

def djget(request):
    name = request.GET['name']
    city = request.GET['city']
    return render(request,"djget.html",locals())

def djpost(request):
    if request.method == 'POST':
        username = request.POST['username']
        password = request.POST['password']
        if username=='david' and password=='1234':
            return HttpResponse('歡迎光臨本網站！')
        else:
            return HttpResponse('帳號或密碼錯誤！')
    else:
        return render(request,"djpost.html",locals())
```
---
## static
```
css
-----------------------------------
.info {
	color:red;
	font-size: 1.5em;
}
-----------------------------------
images
```
## templates
```
dice.html
-----------------------------------
<!DOCTYPE html>
<html>
<head>
    <meta charset='utf-8'>
    <title>擲骰子(二)</title>
</head>
<body>
	<h3> 點數一： {{no1}} </h3>
    <h3> 點數二： {{no2}} </h3>
	<h3> 點數三： {{no3}} </h3>
</body>
</html>

-----------------------------------
djget.html
-----------------------------------
<!DOCTYPE html>
<html>
<head>
    <meta charset='utf-8'>
    <title>傳送 GET 參數</title>
</head>
<body>
	<h1> Django 網站 </h1>
    <h2> 歡迎來自 {{city}} 的 {{name}} 光臨本網站！ </h2>
</body>
</html>
-----------------------------------
djpost.html
-----------------------------------
<!DOCTYPE html>
<html>
<head>
    <meta charset='utf-8'>
    <title>傳送 POST 參數</title>
</head>
<body>
	<h1> Django 網站 </h1>
    <form method='post' action="/djpost">
        {% csrf_token %}
        <p>帳號：<input type='text' name='username' /></p>
        <p>密碼：<input type='text' name='password' /></p>
        <p><button type='submit'>確定</button></p>
    </form>
</body> 
</html>
-----------------------------------
hello3.html
-----------------------------------
<!DOCTYPE html>
<html>
<head>
    <meta charset='utf-8'>
    <title>第一個模版</title>
    {% load staticfiles %}
</head>
<body>
	<h1> 歡迎光臨： {{username}} </h1>
    <h2> 現在時刻： {{now}} </h2>
</body>
</html>
-----------------------------------
hello4.html
-----------------------------------
<!DOCTYPE html>
<html>
<head>
    <meta charset='utf-8'>
    <title>顯示圖片的模版</title>
    {% load staticfiles %}
    <link href="{% static "css/style.css" %}" rel="stylesheet" type="text/css" />
</head>
<body>
    <div id="home">
        <img src="{% static "images/ball.png" %}" alt="歡迎光臨" width="32" height="32" />
  	    <span class="info"> 歡迎光臨： {{username}}</span>
        <h2> 現在時刻： {{now}} </h2>
    </div>   
</body>
</html>
-----------------------------------
show.html
-----------------------------------
<!DOCTYPE html>
<html>
<head>
    <meta charset='utf-8'>
    <title>基本資料</title>
</head>
<body>
    <h3>   
    {% for person in persons%}
       <h2>第 {{forloop.counter}} 位員工</h2>
       <ul>
           <li>姓名：{{person.name}}</li>
           <li>手機：{{person.phone}}</li>
           <li>年齡：{{person.age}}</li>
       </ul>
    {% empty %}
       沒有任何資料
    {% endfor %}  
    </h3>
</body>
</html>
-----------------------------------

```
## db.sqlite3
---
## manage.py
```
#!/usr/bin/env python
"""Django's command-line utility for administrative tasks."""
import os
import sys


def main():
    os.environ.setdefault('DJANGO_SETTINGS_MODULE', 'firstproject.settings')
    try:
        from django.core.management import execute_from_command_line
    except ImportError as exc:
        raise ImportError(
            "Couldn't import Django. Are you sure it's installed and "
            "available on your PYTHONPATH environment variable? Did you "
            "forget to activate a virtual environment?"
        ) from exc
    execute_from_command_line(sys.argv)


if __name__ == '__main__':
    main()

```
# ch18
---
## login
### __pycache__
### __init__.py
---
### settings.py
```
"""
Django settings for login project.

Generated by 'django-admin startproject' using Django 1.11.2.

For more information on this file, see
https://docs.djangoproject.com/en/1.11/topics/settings/

For the full list of settings and their values, see
https://docs.djangoproject.com/en/1.11/ref/settings/
"""

import os

# Build paths inside the project like this: os.path.join(BASE_DIR, ...)
BASE_DIR = os.path.dirname(os.path.dirname(os.path.abspath(__file__)))


# Quick-start development settings - unsuitable for production
# See https://docs.djangoproject.com/en/1.11/howto/deployment/checklist/

# SECURITY WARNING: keep the secret key used in production secret!
SECRET_KEY = '+k@&dhr=jjo5uqj)@#psnnz*u-!tiwl--mh7ed+ucjwks1n-3)'

# SECURITY WARNING: don't run with debug turned on in production!
DEBUG = True

ALLOWED_HOSTS = []


# Application definition

INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth', #確認已加入
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
	'loginapp', # 新增的 app
]

MIDDLEWARE = [
    'django.middleware.security.SecurityMiddleware',
    'django.contrib.sessions.middleware.SessionMiddleware',
    'django.middleware.common.CommonMiddleware',
    'django.middleware.csrf.CsrfViewMiddleware',
    'django.contrib.auth.middleware.AuthenticationMiddleware', #確認已加入
    'django.contrib.messages.middleware.MessageMiddleware',
    'django.middleware.clickjacking.XFrameOptionsMiddleware',
]

ROOT_URLCONF = 'login.urls'

TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [os.path.join(BASE_DIR, 'templates')],  # 加上 templates 路徑
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.debug',
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]

WSGI_APPLICATION = 'login.wsgi.application'


# Database
# https://docs.djangoproject.com/en/1.11/ref/settings/#databases

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': os.path.join(BASE_DIR, 'db.sqlite3'),
    }
}


# Password validation
# https://docs.djangoproject.com/en/1.11/ref/settings/#auth-password-validators

AUTH_PASSWORD_VALIDATORS = [
    {
        'NAME': 'django.contrib.auth.password_validation.UserAttributeSimilarityValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.MinimumLengthValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.CommonPasswordValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.NumericPasswordValidator',
    },
]


# Internationalization
# https://docs.djangoproject.com/en/1.11/topics/i18n/

LANGUAGE_CODE = 'zh-hant'  # 改為繁體中文

TIME_ZONE = 'Asia/Taipei'  # 改為台北時區

USE_I18N = True

USE_L10N = True

USE_TZ = True


# Static files (CSS, JavaScript, Images)
# https://docs.djangoproject.com/en/1.11/howto/static-files/

STATIC_URL = '/static/'
STATICFILES_DIRS = [    # 加入 static 路徑
    os.path.join(BASE_DIR, 'static'),
]
```
### urls.py
```
from django.contrib import admin
from django.urls import path
from loginapp import views

urlpatterns = [
    path('admin/', admin.site.urls),

    path('', views.index),
    path('index/', views.index),

    path('login/', views.login),
    path('logout/', views.logout),	
	
	path('adduser/', views.adduser),	
]
```
### wsgi.py
```
"""
WSGI config for login project.

It exposes the WSGI callable as a module-level variable named ``application``.

For more information on this file, see
https://docs.djangoproject.com/en/1.11/howto/deployment/wsgi/
"""

import os

from django.core.wsgi import get_wsgi_application

os.environ.setdefault("DJANGO_SETTINGS_MODULE", "login.settings")

application = get_wsgi_application()

```
## loginapp
---
### __pycache__
### migrations
---
# ch26
---
## faceRecog1.py
```
from io import BytesIO
from PIL import Image
from matplotlib import patches
import requests
import matplotlib.pyplot as plt

subscription_key = "你的人臉資源key"
face_base_url = "https://southeastasia.api.cognitive.microsoft.com/face/v1.0/"
face_url = face_base_url + 'detect'
image_url = "https://i.imgur.com/G4cZrJ0.jpg"
headers = {'Ocp-Apim-Subscription-Key': subscription_key}
params = {
    'returnFaceId': 'true',
    'returnFaceLandmarks': 'false',
    'returnFaceAttributes': 'age,gender,headPose,smile,facialHair,glasses,emotion,hair,makeup,occlusion,accessories,blur,exposure,noise',
}
data    = {'url': image_url}
response = requests.post(face_url, headers=headers, params=params, json=data)
result = response.json()
#print(result)

#框選臉部及顯示部分資訊
image_file = BytesIO(requests.get(image_url).content)
image = Image.open(image_file)
plt.figure(figsize=(8,8))
ax = plt.imshow(image)
for face in result:
     fr = face["faceRectangle"]  #取得臉部坐標
     fa = face["faceAttributes"]  #取得臉部屬性
     origin = (fr["left"], fr["top"])
     p = patches.Rectangle(origin, fr["width"], fr["height"], fill=False, linewidth=2, color='b')  #畫出矩形
     ax.axes.add_patch(p)
     plt.text(origin[0], origin[1], "%s, %d"%(fa["gender"], fa["age"]), fontsize=20, weight="bold", va="bottom", color='r')  #顯示資訊
plt.axis("off")

```
## faceVerify1.py
```
def getFaceId(image_url):  #取得臉部Id
    face_url = face_base_url + 'detect'
    params = {
        'returnFaceId': 'true',
        'returnFaceLandmarks': 'false',
        'returnFaceAttributes': 'age',
    }
    data    = {'url': image_url}
    response = requests.post(face_url, headers=headers, params=params, json=data)
    faces = response.json()
    return faces[0]['faceId']

def verifyFace(faceid1, faceid2):  #比對臉部是否相同
    face_url = face_base_url + 'verify'
    data    = {
        'faceId1': faceid1,
        'faceId2': faceid2,
    }
    response = requests.post(face_url, headers=headers, json=data)
    result = response.json()
    #print(result)
    if result['isIdentical']== True:  #臉部相同
        return '兩張相片為同一人！'
    else:  #臉部不同
        return '兩張相片為不同人！'  

import requests

subscription_key = "你的人臉資源key"
face_base_url = "https://southeastasia.api.cognitive.microsoft.com/face/v1.0/"
headers = {'Ocp-Apim-Subscription-Key': subscription_key}

jengid1 = getFaceId("https://i.imgur.com/JKKvMiP.jpg")  #jeng照片一
jengid2 = getFaceId("https://i.imgur.com/dtusSZ1.jpg")  #jeng照片二
davidid1 = getFaceId("https://i.imgur.com/o4boWWG.jpg")  #david照片
print('傳入相同人員的不同照片：' + verifyFace(jengid1, jengid2))
print('\n傳入不同人員的照片：' + verifyFace(jengid1, davidid1))
```
## imgAnalyze1.py
```
import requests
import matplotlib.pyplot as plt
from PIL import Image
from io import BytesIO

subscription_key = "你的電腦視覺資源key"
vision_base_url = "https://southeastasia.api.cognitive.microsoft.com/vision/v2.0/"
analyze_url = vision_base_url + "analyze"
image_url = "https://i.imgur.com/BO7tlY7.jpg"
headers = {'Ocp-Apim-Subscription-Key': subscription_key }
params  = {'visualFeatures': 'Categories,Description,Color'}
data    = {'url': image_url}
response = requests.post(analyze_url, headers=headers, params=params, json=data)
analysis = response.json()
#print(analysis)

#顯示圖片及圖片描述
image_caption = analysis["description"]["captions"][0]["text"]  #取得圖片描述
image = Image.open(BytesIO(requests.get(image_url).content))
plt.imshow(image)
plt.axis("off")
_ = plt.title(image_caption, size="x-large", y=-0.1)  #顯示圖片描述

```
## imgAnalyze2.py
```
import requests
import matplotlib.pyplot as plt
from PIL import Image
from io import BytesIO

subscription_key = "你的電腦視覺資源key"
vision_base_url = "https://southeastasia.api.cognitive.microsoft.com/vision/v2.0/"
analyze_url = vision_base_url + "analyze"
image_path = "street.jpg"  #本機圖片檔路徑
image_data = open(image_path, "rb").read()  #讀取圖片檔
headers = {'Ocp-Apim-Subscription-Key': subscription_key,
           'Content-Type': 'application/octet-stream'}
params = {'visualFeatures': 'Categories,Description,Color'}
response = requests.post(analyze_url, headers=headers, params=params, data=image_data)
analysis = response.json()
#print(analysis)

#顯示圖片及圖片描述
image_caption = analysis["description"]["captions"][0]["text"]
image = Image.open(BytesIO(image_data))
plt.imshow(image)
plt.axis("off")
_ = plt.title(image_caption, size="x-large", y=-0.1)

```
## landmark1.py
```
import requests
import matplotlib.pyplot as plt
from PIL import Image
from io import BytesIO

subscription_key = "你的電腦視覺資源key"
vision_base_url = "https://southeastasia.api.cognitive.microsoft.com/vision/v2.0/"
landmark_analyze_url = vision_base_url + "models/landmarks/analyze"
image_url = "https://i.imgur.com/WNlkY79.jpg"  #台北101
headers = {'Ocp-Apim-Subscription-Key': subscription_key}
params  = {'model': 'landmarks'}
data    = {'url': image_url}
response = requests.post(landmark_analyze_url, headers=headers, params=params, json=data)
analysis = response.json()
#print(analysis)

if len(analysis["result"]["landmarks"]) > 0:  #如果有地標
    landmark_name = analysis["result"]["landmarks"][0]["name"]  #取得地標名稱
    image = Image.open(BytesIO(requests.get(image_url).content))
    plt.imshow(image)
    plt.axis("off")
    _ = plt.title(landmark_name, size="x-large", y=-0.1)
else:  #未傳回地標
    print("無法辨識地標")
    
```
## landmark2.py
```
import requests
import matplotlib.pyplot as plt
from PIL import Image
from io import BytesIO

subscription_key = "你的電腦視覺資源key"
vision_base_url = "https://southeastasia.api.cognitive.microsoft.com/vision/v2.0/"
landmark_analyze_url = vision_base_url + "models/landmarks/analyze"
image_url = "https://i.imgur.com/sx3xwOq.jpg"  #歐巴馬
headers = {'Ocp-Apim-Subscription-Key': subscription_key}
params  = {'model': 'celebrities'}
data    = {'url': image_url}
response = requests.post(landmark_analyze_url, headers=headers, params=params, json=data)
analysis = response.json()
#print(analysis)

if len(analysis["result"]["celebrities"]) > 0:  #如果有名人
    landmark_name = analysis["result"]["celebrities"][0]["name"]  #取得名人資訊
    image = Image.open(BytesIO(requests.get(image_url).content))
    plt.imshow(image)
    plt.axis("off")
    _ = plt.title(landmark_name, size="x-large", y=-0.1)
else:  #未傳回地標
    print("無法辨識地標")
    
```
## language1.py
```
import requests

subscription_key = "你的翻譯文字資源key"
trans_base_url = "https://api.cognitive.microsofttranslator.com/"
trans_url = trans_base_url + 'detect?api-version=3.0'
headers = {'Ocp-Apim-Subscription-Key': subscription_key}
while True:
    textinput = input('輸入文句 (直接按 Enter 鍵就結束程式)：')
    if textinput != '':
        data    = [{'text' : textinput}]
        response = requests.post(trans_url, headers=headers, json=data)
        result = response.json()
        print('輸入文句語言：' + result[0]['language'])
        #print(result)
    else:
        break

```
## ocr1.py
```
import requests
import matplotlib.pyplot as plt
from matplotlib.patches import Rectangle
from PIL import Image
from io import BytesIO

subscription_key = "你的電腦視覺資源key"  #資源key
vision_base_url = "https://southeastasia.api.cognitive.microsoft.com/vision/v2.0/"  #資源端點
ocr_url = vision_base_url + "ocr"  #功能為ocr
image_url = "https://i.imgur.com/ptMvd6w.png"  #遠端圖片
headers = {'Ocp-Apim-Subscription-Key': subscription_key}
params  = {'language': 'unk', 'detectOrientation': 'true'}  #自動偵測文字類別及方向
data    = {'url': image_url}
response = requests.post(ocr_url, headers=headers, params=params, json=data)
analysis = response.json()
#print(analysis)  #列印結果

#line_infos串列儲存所有文字的坐標
line_infos = []
for region in analysis["regions"]:
    line_infos.append(region["lines"])
word_infos = []
for line in line_infos:
    for word_metadata in line:
        for word_info in word_metadata["words"]:
            word_infos.append(word_info)
#框選所有文字
plt.figure(figsize=(12, 12))
image = Image.open(BytesIO(requests.get(image_url).content))
ax = plt.imshow(image, alpha=0.5)
for word in word_infos:
    bbox = [int(num) for num in word["boundingBox"].split(",")]
    #text = word["text"]
    origin = (bbox[0], bbox[1])
    patch  = Rectangle(origin, bbox[2], bbox[3], fill=False, linewidth=2, color='r')
    ax.axes.add_patch(patch)
plt.axis("off")  #隱藏坐標軸

```
## ocr2.py
```
import requests
import time
import matplotlib.pyplot as plt
from matplotlib.patches import Polygon
from PIL import Image
from io import BytesIO

subscription_key = "你的電腦視覺資源key"
vision_base_url = "https://southeastasia.api.cognitive.microsoft.com/vision/v2.0/"
text_recognition_url = vision_base_url + "read/core/asyncBatchAnalyze"
image_url = "https://i.imgur.com/VYLTAUV.jpg"
headers = {'Ocp-Apim-Subscription-Key': subscription_key}
params  = {'mode': 'Handwritten'}
data    = {'url': image_url}
response = requests.post(text_recognition_url, headers=headers, params=params, json=data)

analysis = {}
flag = True  #記錄是否辨識完成,False為辨識完成
while (flag):
    response_final = requests.get(response.headers["Operation-Location"], headers=headers)
    analysis = response_final.json()  #取得回傳值
    #print(analysis)  #顯示回傳值
    if ("recognitionResults" in analysis): flag= False  #回傳值有「recognitionResults」表示完成
    if ("status" in analysis and analysis['status'] == 'Failed'): flag= False  #辨識失敗
    time.sleep(1)  #辨識需時間,每1秒讀一次回傳值

polygons=[]  #取得每列坐標
if ("recognitionResults" in analysis):
    polygons = []
    for line in analysis["recognitionResults"][0]["lines"]:
        polygons.append((line["boundingBox"], line["text"]))

#框選及列印每列文字
plt.figure(figsize=(12, 12))
image = Image.open(BytesIO(requests.get(image_url).content))
ax = plt.imshow(image)
for polygon in polygons:
    vertices = []
    for i in range(0, len(polygon[0]), 2):
        vertices.append((polygon[0][i], polygon[0][i+1]))
    text = polygon[1]  #取得文字
    patch = Polygon(vertices, closed=True, fill=False, linewidth=2, color='r')
    ax.axes.add_patch(patch)
    plt.text(vertices[0][0], vertices[0][1], text, fontsize=20, va="top", color='b')  #列印文字
plt.axis("off")
```
## translate1.py
```
import requests

subscription_key = "你的翻譯文字資源key"
trans_base_url = "https://api.cognitive.microsofttranslator.com/"
trans_url = trans_base_url + 'translate?api-version=3.0'
headers = {'Ocp-Apim-Subscription-Key': subscription_key}
params = '&to=en'  #翻譯為英文
while True:
    textinput = input('輸入文句 (直接按 Enter 鍵就結束程式)：')
    if textinput != '':
        data    = [{'text' : textinput}]
        response = requests.post(trans_url, headers=headers, params=params, json=data)
        result = response.json()
        print('翻譯結果：' + result[0]['translations'][0]['text'])
        #print(result)
    else:
        break
```
# ch27
---
## jieba1.py
```
import jieba

sentence = '我今天要到台北松山機場出差！'
breakword = jieba.cut(sentence)
print('|'.join(breakword))   

```
## jieba2.py
```
import jieba

sentence = '我今天要到台北松山機場出差！'
breakword = jieba.cut(sentence, cut_all=False)
print('精確模式：' + '|'.join(breakword))   

breakword = jieba.cut(sentence, cut_all=True)
print('全文模式：' + '|'.join(breakword))   

breakword = jieba.cut_for_search(sentence)
print('搜索引擎模式：' + '|'.join(breakword))   

```
## jieba3.py
```
import jieba

jieba.set_dictionary('dictionary/dict.txt.big.txt')  #設定繁體中文詞庫

sentence = '我今天要到台北松山機場出差！'
breakword = jieba.cut(sentence, cut_all=False)
print('|'.join(breakword))   

```
## jieba4.py
```
import jieba

jieba.set_dictionary('dictionary/dict.txt.big.txt')

sentence = '今天是元旦，總統蔡英文發表了元旦文告。'
breakword = jieba.cut(sentence, cut_all=False)
print('|'.join(breakword))   

```
## jieba5.py
```
import jieba

jieba.set_dictionary('dictionary/dict.txt.big.txt')
jieba.load_userdict('dictionary/user_dict_test.txt')  #設定自訂詞庫

sentence = '今天是元旦，總統蔡英文發表了元旦文告。'
breakword = jieba.cut(sentence, cut_all=False)
print('|'.join(breakword))   

```
## jieba6.py
```
import jieba

jieba.set_dictionary('dictionary/dict.txt.big.txt')
jieba.load_userdict('dictionary/user_dict_test.txt')
with open('dictionary/stopWord_test.txt', 'r', encoding='utf-8-sig') as f:  #設定停用詞
    stops = f.read().split('\n')   

sentence = '今天是元旦，總統蔡英文發表了元旦文告。'
breakword = jieba.cut(sentence, cut_all=False)
words = []
for word in breakword:  #拆解句子為字詞
    if word not in stops:  #不是停用詞
        words.append(word)
print('|'.join(words)) 

```
## newsCloud1.py
```
from PIL import Image
import matplotlib.pyplot as plt
from wordcloud import WordCloud
import jieba
import numpy as np
from collections import Counter

text = open('news1.txt', "r",encoding="utf-8").read()  #讀文字資料
 
jieba.set_dictionary('dictionary/dict.txt.big.txt')
with open('dictionary/stopWord_cloud.txt', 'r', encoding='utf-8-sig') as f:  #設定停用詞
#with open('dictionary/stopWord_cloudmod.txt', 'r', encoding='utf-8-sig') as f:  #設定停用詞
    stops = f.read().split('\n')   
terms = []  #儲存字詞
for t in jieba.cut(text, cut_all=False):  #拆解句子為字詞
    if t not in stops:  #不是停用詞
        terms.append(t)
diction = Counter(terms)

font = 'msch.ttf'  #設定字型
#mask = np.array(Image.open("heart.png"))  #設定文字雲形狀 
wordcloud = WordCloud(font_path=font) 
#wordcloud = WordCloud(background_color="white",mask=mask,font_path=font)  #背景顏色預設黑色,改為白色 
wordcloud.generate_from_frequencies(frequencies=diction)  #產生文字雲

#產生圖片
plt.figure(figsize=(6,6))
plt.imshow(wordcloud)
plt.axis("off")
plt.show()

wordcloud.to_file("news_Wordcloud.png")  #存檔

```
## newsCloud2.py
```
from PIL import Image
import matplotlib.pyplot as plt
from wordcloud import WordCloud
import jieba
import numpy as np
from collections import Counter

text = open('news1.txt', "r",encoding="utf-8").read()  #讀文字資料
 
jieba.set_dictionary('dictionary/dict.txt.big.txt')
#with open('dictionary/stopWord_cloud.txt', 'r', encoding='utf-8-sig') as f:  #設定停用詞
with open('dictionary/stopWord_cloudmod.txt', 'r', encoding='utf-8-sig') as f:  #設定停用詞
    stops = f.read().split('\n')   
terms = []  #儲存字詞
for t in jieba.cut(text, cut_all=False):  #拆解句子為字詞
    if t not in stops:  #不是停用詞
        terms.append(t)
diction = Counter(terms)

font = 'msch.ttf'  #設定字型
mask = np.array(Image.open("heart.png"))  #設定文字雲形狀 
#wordcloud = WordCloud(font_path=font) 
wordcloud = WordCloud(background_color="white",mask=mask,font_path=font)  #背景顏色預設黑色,改為白色 
wordcloud.generate_from_frequencies(frequencies=diction)  #產生文字雲

#產生圖片
plt.figure(figsize=(6,6))
plt.imshow(wordcloud)
plt.axis("off")
plt.show()

wordcloud.to_file("news_Wordcloud.png")  #存檔

```
## unionNews.py
```
import requests
from bs4 import BeautifulSoup as soup
from PIL import Image
import matplotlib.pyplot as plt
from wordcloud import WordCloud
import jieba
import numpy as np
from collections import Counter

urls = []
url = 'https://udn.com/news/breaknews/1'  #聯合報新聞
html = requests.get(url)
sp = soup(html.text, 'html.parser')
data1 = sp.select('#breaknews_body dl dt h2 a')
for d in data1:  #取得新聞連結
    urls.append('https://udn.com' + d.get('href'))

text_news = ''
i = 1
for url in urls:  #逐一取得新聞
    html = requests.get(url)
    sp = soup(html.text, 'html.parser')
    data1 = sp.select('#story_body_content p')  #新聞內容
    print('處理第 {} 則新聞'.format(i))
    for d in data1:
        if d.text.find('延伸閱讀') != -1:  #遇到延伸閱讀就結束此則新聞
            break
        if d.text != '':  #有新聞內容
            text_news += d.text
    i += 1
 
jieba.set_dictionary('dictionary/dict.txt.big.txt')
with open('dictionary/stopWord_union.txt', 'r', encoding='utf-8-sig') as f:  #設定停用詞
    stops = f.read().split('\n')   
terms = []  #儲存字詞
for t in jieba.cut(text_news, cut_all=False):  #拆解句子為字詞
    if t not in stops:  #不是停用詞
        terms.append(t)
diction = Counter(terms)

font = 'msch.ttf'  #設定字型
mask = np.array(Image.open("heart.png"))  #設定文字雲形狀 
unioncloud = WordCloud(background_color="white",mask=mask,font_path=font)  #背景顏色預設黑色,改為白色 
unioncloud.generate_from_frequencies(frequencies=diction)  #產生文字雲

#產生圖片
plt.figure(figsize=(6,6))
plt.imshow(unioncloud)
plt.axis("off")
plt.show()

unioncloud.to_file("union_Wordcloud.png")  #存檔

```
# ch28
---
## Led_Blink.py
```
from machine import Pin
import time 
 
# DPIO16對應到D0 
led = Pin(16, Pin.OUT)
 
while True:
    led.value(1)   #燈亮
    time.sleep(0.5)#暫停 0.5 秒

    led.value(0)   #燈熄
    time.sleep(0.5)#暫停 0.5 秒
    print("Hello")
```
## main.py
```
from machine import Pin
import time 
 
# DPIO2對應到D4 
led = Pin(2, Pin.OUT) #D4 內建 Led
 
while True:
    led.value(1)   #燈熄
    time.sleep(0.5)#暫停 0.5 秒

    led.value(0)   #燈亮
    time.sleep(0.5)#暫停 0.5 秒
    print("Hello")
```
# ch29
---
## adc_pwm.py
```
from machine import Pin,ADC,PWM
import time

led = PWM(Pin(2), freq=1000) #DPIO2對應到D4
a0 = ADC(0) 

while True:
  value = a0.read() #讀取A0埠
  print(value)      #顯示轉換後的數值
  led.duty(value)   #亮度
  time.sleep(0.1) 
```
## button.py
```
from machine import Pin
from time import sleep
 
# DPIO2對應到D4 
ledB = Pin(2, Pin.OUT)  #D4 內建 Led
button = Pin(0, Pin.IN) #GPIO0--D3

while True:
    if button.value()==0: #按下按鈕，燈亮
        ledB.value(0)
    else:  #放開按鈕，燈熄
        ledB.value(1)
    print(button.value())
    sleep(.1)    
```
## buzzer.py
```
from machine import Pin, PWM
import time

buzzer = PWM(Pin(14, Pin.OUT), duty=900) # D5

def sound(): 
    buzzer.freq(400)
    time.sleep(0.5)
    buzzer.freq(700)
    time.sleep(0.5)

try:
    for i in range(5):
        sound()
    buzzer.deinit()
except:  # CTRL + C 中斷
    buzzer.deinit()
        

```
## led_turn.py
```
from machine import Pin
import time 

def show_led(led):
    led.value(1)    #燈亮
    time.sleep(0.5) # 停0.5秒
    led.value(0)    #燈熄
 
# GPIO16對應到D0，DPIO14對應到D5，GPIO12對應到D6 
ledR = Pin(16, Pin.OUT)  #D0 紅燈
ledG = Pin(14, Pin.OUT)  #D5 綠燈
ledB = Pin(12, Pin.OUT)  #D6 藍燈
 
while True:
    show_led(ledR) # 紅燈亮
    show_led(ledG) # 綠燈亮
    show_led(ledB) # 藍燈亮
    print("R,G,B")
```
## light_sensor.py
```
from machine import Pin,ADC
import time

led = Pin(2, Pin.OUT) #DPIO2對應到D4
a0 = ADC(0) 

while True:
  value = a0.read() #讀取A0埠
  print(value)      #顯示轉換後的數值
  if value<600:
      led.value(0)  #開燈
  else:
      led.value(1)  #關燈
  time.sleep(0.1) 
```
## music.py
```
from machine import Pin, PWM
import time

pitches = {
    'C':261, # D0
    'D':294, # Re
    'E':329, # Mi
    'F':349, # Fa
    'G':392, # So
    'A':440, # La
    'B':493, # Si
    'S':0    # Stop
}

music = (
    ('C',1),('C',1),('G',1),('G',1),('A',1),('A',1),('G',2),
    ('F',1),('F',1),('E',1),('E',1),('D',1),('D',1),('C',2),
    ('G',1),('G',1),('F',1),('F',1),('E',1),('E',1),('D',2),
    ('G',1),('G',1),('F',1),('F',1),('E',1),('E',1),('D',2),
    ('C',1),('C',1),('G',1),('G',1),('A',1),('A',1),('G',2),
    ('F',1),('F',1),('E',1),('E',1),('D',1),('D',1),('C',1)
)

speed=400 # 設定節拍速度
period=10 # 設定每拍停頓時間

buzzer = PWM(Pin(14, Pin.OUT), duty=1000) # D5
try:
    for tone,tempo in music:
        if (tone=="S"):
            buzzer.duty(0) # 靜音
        else:
            buzzer.duty(1000)
            buzzer.freq(pitches[tone])
        time.sleep_ms(tempo*speed)
        print(pitches[tone])
        #以靜音設定每拍間稍為停頓
        buzzer.duty(0)         # 靜音
        time.sleep_ms(period)  # 停頓時間
    buzzer.deinit()
except:  # CTRL + C 中斷
    buzzer.deinit()       

```
## neon.py
```
from machine import Pin,PWM
import time
import random
 
pwmR = PWM(Pin(13),freq=1000) #D7 紅燈
pwmG = PWM(Pin(14),freq=1000) #D5 綠燈
pwmB = PWM(Pin(12),freq=1000) #D6 藍燈

while True:
    R= random.randint(0,1023) # 產生 0~1023 的亂數
    G= random.randint(0,1023) # 產生 0~1023 的亂數
    B= random.randint(0,1023) # 產生 0~1023 的亂數

    pwmR.duty(R)
    time.sleep(0.1)
    pwmG.duty(G)
    time.sleep(0.1)
    pwmB.duty(B)
    time.sleep(0.1)    
    print(R,G,B)



```
## pwm.py
```
from machine import Pin, PWM
import time
 
led = PWM(Pin(2),freq=1000) # DPIO2對應到D4 

while True:
    for n in range(1023,-1,-1): #燈漸亮
        led.duty(n)
        time.sleep_ms(5)
    for n in range(1024):      #燈漸熄
        led.duty(n)
        time.sleep_ms(5)
    print("change")
```
## random.py
```
### Start of file: random.py ###
import os

def getrandbits(k):
    numbytes = (k + 7) // 8
    x = int.from_bytes(os.urandom(numbytes), 'big')
    return x >> (numbytes * 8 - k)

def bit_length(n):
    res = n
    count = 1
    while res>1:
        res = res>>1
        count = count+1
    return count

def randbelow(n):
    k = bit_length(n)
    r = getrandbits(k)
    while r >= n:
        r = getrandbits(k)
    return r

def randrange(start, stop=None, step=1):
    istart = int(start)
    if istart != start:
        raise ValueError("non-integer arg 1 for randrange()")
    if stop is None:
        if istart > 0:
            return randbelow(istart)
        raise ValueError("empty range for randrange()")

    # stop argument supplied.
    istop = int(stop)
    if istop != stop:
        raise ValueError("non-integer stop for randrange()")
    width = istop - istart
    if step == 1 and width > 0:
        return istart + randbelow(width)
    if step == 1:
        raise ValueError("empty range for randrange() (%d,%d, %d)" % (istart, istop, width))

    # Non-unit step argument supplied.
    istep = int(step)
    if istep != step:
        raise ValueError("non-integer step for randrange()")
    if istep > 0:
        n = (width + istep - 1) // istep
    elif istep < 0:
        n = (width + istep + 1) // istep
    else:
        raise ValueError("zero step for randrange()")

    if n <= 0:
        raise ValueError("empty range for randrange()")

    return istart + istep*randbelow(n)

def randint(a, b):
    return randrange(a, b+1)
### End of file random.py ###

```
# ch30
---
## dht11.py
```
from machine import Pin,Timer
import dht,time     

temp,hum=0,0
d = dht.DHT11(Pin(0)) #在D3建立DHT11物件
led = Pin(2, Pin.OUT) #D4內建Led

def readdht(t):
    global temp,hum
    try:
        d.measure()  #重新測量溫溼度
        temp=d.temperature()       #讀取攝氏溫度
        hum=d.humidity()           #讀取相對溼度
        print("溫    度: %3.1f °C" % temp)
        print("相對溼度: %3.1f %% RH" % hum)
    except:
        print('讀取不正常!')  

timer = Timer(1)
timer.init(period=2000, mode=Timer.PERIODIC, callback=readdht)

try:
    while True:
        if temp>24: # 溫度>24度，開燈
            led.value(0)
        else: # 溫度<24度，熄燈
            led.value(1)
        time.sleep(0.1) #暫停 0.1 秒
except:
    timer.deinit()
    print('stopped')  
```
## HCSR04.py
```
from machine import Pin
import machine,time

echoTimeout = 23200 #等待截止時間
trigPin = Pin(13, mode=Pin.OUT) #觸發腳位 D7
echoPin = Pin(15, mode=Pin.IN)  #回應腳位 D8
trigPin.value(0)

def distance():
    trigPin.value(1) # 送出 10 us 的觸發訊號
    time.sleep_us(10)
    trigPin.value(0)
    # 計算高電位脈衝的時間
    pulseTime = machine.time_pulse_us(echoPin, 1, echoTimeout)
    if pulseTime > 0:
        return pulseTime / 58  # 公分換算
    else:
        return pulseTime  # 傳回 -1或-2

while True:
    cm = distance()
    if cm > 0:
        print('距離:%5.1f 公分' % cm)        
    else:
        print('讀取異常!')        
    time.sleep(1)  
    
```
## timer01.py
```
from machine import Pin,Timer
import time 

led = Pin(2, Pin.OUT) # DPIO2(D4)內建Led

def show(t):
    toggle=not led.value()    
    led.value(toggle)   #燈閃爍           

timer = Timer(1)
timer.init(period=500, mode=Timer.PERIODIC, callback=show)

try:
    while True:
        for n in range(100):
            print(n)
            time.sleep(0.1)
except:
    timer.deinit()
    print('stopped')
```
## timer02.py
```
from machine import Pin,Timer
import time 

led = Pin(2, Pin.OUT) # DPIO2(D4)內建Led
timer = Timer(1)
counter=0

def show(t):
    global counter
    counter+=1
    led.value(not led.value())   #燈閃爍
    if counter==10:
        t.deinit()    

timer.init(period=500, mode=Timer.PERIODIC, callback=show)    

try:
    while True:
        pass
except:
    timer.deinit()
    print('stopped')
```
# ch31
---
## esp8266_i2c_lcd.py
```
"""Implements a HD44780 character LCD connected via PCF8574 on I2C.
   This was tested with: https://www.wemos.cc/product/d1-mini.html"""

from lcd_api import LcdApi
from machine import I2C
from time import sleep_ms

# The PCF8574 has a jumper selectable address: 0x20 - 0x27
DEFAULT_I2C_ADDR = 0x27

# Defines shifts or masks for the various LCD line attached to the PCF8574

MASK_RS = 0x01
MASK_RW = 0x02
MASK_E = 0x04
SHIFT_BACKLIGHT = 3
SHIFT_DATA = 4


class I2cLcd(LcdApi):
    """Implements a HD44780 character LCD connected via PCF8574 on I2C."""

    def __init__(self, i2c, i2c_addr, num_lines, num_columns):
        self.i2c = i2c
        self.i2c_addr = i2c_addr
        self.i2c.writeto(self.i2c_addr, bytearray([0]))
        sleep_ms(20)   # Allow LCD time to powerup
        # Send reset 3 times
        self.hal_write_init_nibble(self.LCD_FUNCTION_RESET)
        sleep_ms(5)    # need to delay at least 4.1 msec
        self.hal_write_init_nibble(self.LCD_FUNCTION_RESET)
        sleep_ms(1)
        self.hal_write_init_nibble(self.LCD_FUNCTION_RESET)
        sleep_ms(1)
        # Put LCD into 4 bit mode
        self.hal_write_init_nibble(self.LCD_FUNCTION)
        sleep_ms(1)
        LcdApi.__init__(self, num_lines, num_columns)
        cmd = self.LCD_FUNCTION
        if num_lines > 1:
            cmd |= self.LCD_FUNCTION_2LINES
        self.hal_write_command(cmd)

    def hal_write_init_nibble(self, nibble):
        """Writes an initialization nibble to the LCD.

        This particular function is only used during initialization.
        """
        byte = ((nibble >> 4) & 0x0f) << SHIFT_DATA
        self.i2c.writeto(self.i2c_addr, bytearray([byte | MASK_E]))
        self.i2c.writeto(self.i2c_addr, bytearray([byte]))

    def hal_backlight_on(self):
        """Allows the hal layer to turn the backlight on."""
        self.i2c.writeto(self.i2c_addr, bytearray([1 << SHIFT_BACKLIGHT]))

    def hal_backlight_off(self):
        """Allows the hal layer to turn the backlight off."""
        self.i2c.writeto(self.i2c_addr, bytearray([0]))

    def hal_write_command(self, cmd):
        """Writes a command to the LCD.

        Data is latched on the falling edge of E.
        """
        byte = ((self.backlight << SHIFT_BACKLIGHT) | (((cmd >> 4) & 0x0f) << SHIFT_DATA))
        self.i2c.writeto(self.i2c_addr, bytearray([byte | MASK_E]))
        self.i2c.writeto(self.i2c_addr, bytearray([byte]))
        byte = ((self.backlight << SHIFT_BACKLIGHT) | ((cmd & 0x0f) << SHIFT_DATA))
        self.i2c.writeto(self.i2c_addr, bytearray([byte | MASK_E]))
        self.i2c.writeto(self.i2c_addr, bytearray([byte]))
        if cmd <= 3:
            # The home and clear commands require a worst case delay of 4.1 msec
            sleep_ms(5)

    def hal_write_data(self, data):
        """Write data to the LCD."""
        byte = (MASK_RS | (self.backlight << SHIFT_BACKLIGHT) | (((data >> 4) & 0x0f) << SHIFT_DATA))
        self.i2c.writeto(self.i2c_addr, bytearray([byte | MASK_E]))
        self.i2c.writeto(self.i2c_addr, bytearray([byte]))
        byte = (MASK_RS | (self.backlight << SHIFT_BACKLIGHT) | ((data & 0x0f) << SHIFT_DATA))
        self.i2c.writeto(self.i2c_addr, bytearray([byte | MASK_E]))
        self.i2c.writeto(self.i2c_addr, bytearray([byte]))

```
## i2cscan.py
```
from machine import Pin,I2C
i2c = I2C(scl=Pin(13), sda=Pin(12), freq=100000)
print(i2c.scan())


```
## lcd_api.py
```
"""Provides an API for talking to HD44780 compatible character LCDs."""

import time

class LcdApi:
    """Implements the API for talking with HD44780 compatible character LCDs.
    This class only knows what commands to send to the LCD, and not how to get
    them to the LCD.

    It is expected that a derived class will implement the hal_xxx functions.
    """

    # The following constant names were lifted from the avrlib lcd.h
    # header file, however, I changed the definitions from bit numbers
    # to bit masks.
    #
    # HD44780 LCD controller command set

    LCD_CLR = 0x01              # DB0: clear display
    LCD_HOME = 0x02             # DB1: return to home position

    LCD_ENTRY_MODE = 0x04       # DB2: set entry mode
    LCD_ENTRY_INC = 0x02        # --DB1: increment
    LCD_ENTRY_SHIFT = 0x01      # --DB0: shift

    LCD_ON_CTRL = 0x08          # DB3: turn lcd/cursor on
    LCD_ON_DISPLAY = 0x04       # --DB2: turn display on
    LCD_ON_CURSOR = 0x02        # --DB1: turn cursor on
    LCD_ON_BLINK = 0x01         # --DB0: blinking cursor

    LCD_MOVE = 0x10             # DB4: move cursor/display
    LCD_MOVE_DISP = 0x08        # --DB3: move display (0-> move cursor)
    LCD_MOVE_RIGHT = 0x04       # --DB2: move right (0-> left)

    LCD_FUNCTION = 0x20         # DB5: function set
    LCD_FUNCTION_8BIT = 0x10    # --DB4: set 8BIT mode (0->4BIT mode)
    LCD_FUNCTION_2LINES = 0x08  # --DB3: two lines (0->one line)
    LCD_FUNCTION_10DOTS = 0x04  # --DB2: 5x10 font (0->5x7 font)
    LCD_FUNCTION_RESET = 0x30   # See "Initializing by Instruction" section

    LCD_CGRAM = 0x40            # DB6: set CG RAM address
    LCD_DDRAM = 0x80            # DB7: set DD RAM address

    LCD_RS_CMD = 0
    LCD_RS_DATA = 1

    LCD_RW_WRITE = 0
    LCD_RW_READ = 1

    def __init__(self, num_lines, num_columns):
        self.num_lines = num_lines
        if self.num_lines > 4:
            self.num_lines = 4
        self.num_columns = num_columns
        if self.num_columns > 40:
            self.num_columns = 40
        self.cursor_x = 0
        self.cursor_y = 0
        self.backlight = True
        self.display_off()
        self.backlight_on()
        self.clear()
        self.hal_write_command(self.LCD_ENTRY_MODE | self.LCD_ENTRY_INC)
        self.hide_cursor()
        self.display_on()

    def clear(self):
        """Clears the LCD display and moves the cursor to the top left
        corner.
        """
        self.hal_write_command(self.LCD_CLR)
        self.hal_write_command(self.LCD_HOME)
        self.cursor_x = 0
        self.cursor_y = 0

    def show_cursor(self):
        """Causes the cursor to be made visible."""
        self.hal_write_command(self.LCD_ON_CTRL | self.LCD_ON_DISPLAY |
                               self.LCD_ON_CURSOR)

    def hide_cursor(self):
        """Causes the cursor to be hidden."""
        self.hal_write_command(self.LCD_ON_CTRL | self.LCD_ON_DISPLAY)

    def blink_cursor_on(self):
        """Turns on the cursor, and makes it blink."""
        self.hal_write_command(self.LCD_ON_CTRL | self.LCD_ON_DISPLAY |
                               self.LCD_ON_CURSOR | self.LCD_ON_BLINK)

    def blink_cursor_off(self):
        """Turns on the cursor, and makes it no blink (i.e. be solid)."""
        self.hal_write_command(self.LCD_ON_CTRL | self.LCD_ON_DISPLAY |
                               self.LCD_ON_CURSOR)

    def display_on(self):
        """Turns on (i.e. unblanks) the LCD."""
        self.hal_write_command(self.LCD_ON_CTRL | self.LCD_ON_DISPLAY)

    def display_off(self):
        """Turns off (i.e. blanks) the LCD."""
        self.hal_write_command(self.LCD_ON_CTRL)

    def backlight_on(self):
        """Turns the backlight on.

        This isn't really an LCD command, but some modules have backlight
        controls, so this allows the hal to pass through the command.
        """
        self.backlight = True
        self.hal_backlight_on()

    def backlight_off(self):
        """Turns the backlight off.

        This isn't really an LCD command, but some modules have backlight
        controls, so this allows the hal to pass through the command.
        """
        self.backlight = False
        self.hal_backlight_off()

    def move_to(self, cursor_x, cursor_y):
        """Moves the cursor position to the indicated position. The cursor
        position is zero based (i.e. cursor_x == 0 indicates first column).
        """
        self.cursor_x = cursor_x
        self.cursor_y = cursor_y
        addr = cursor_x & 0x3f
        if cursor_y & 1:
            addr += 0x40    # Lines 1 & 3 add 0x40
        if cursor_y & 2:
            addr += 0x14    # Lines 2 & 3 add 0x14
        self.hal_write_command(self.LCD_DDRAM | addr)

    def putchar(self, char):
        """Writes the indicated character to the LCD at the current cursor
        position, and advances the cursor by one position.
        """
        if char != '\n':
            self.hal_write_data(ord(char))
            self.cursor_x += 1
        if self.cursor_x >= self.num_columns or char == '\n':
            self.cursor_x = 0
            self.cursor_y += 1
            if self.cursor_y >= self.num_lines:
                self.cursor_y = 0
            self.move_to(self.cursor_x, self.cursor_y)

    def putstr(self, string):
        """Write the indicated string to the LCD at the current cursor
        position and advances the cursor position appropriately.
        """
        for char in string:
            self.putchar(char)

    def custom_char(self, location, charmap):
        """Write a character to one of the 8 CGRAM locations, available
        as chr(0) through chr(7).
        """
        location &= 0x7
        self.hal_write_command(self.LCD_CGRAM | (location << 3))
        self.hal_sleep_us(40)
        for i in range(8):
            self.hal_write_data(charmap[i])
            self.hal_sleep_us(40)
        self.move_to(self.cursor_x, self.cursor_y)

    def hal_backlight_on(self):
        """Allows the hal layer to turn the backlight on.

        If desired, a derived HAL class will implement this function.
        """
        pass

    def hal_backlight_off(self):
        """Allows the hal layer to turn the backlight off.

        If desired, a derived HAL class will implement this function.
        """
        pass

    def hal_write_command(self, cmd):
        """Write a command to the LCD.

        It is expected that a derived HAL class will implement this
        function.
        """
        raise NotImplementedError

    def hal_write_data(self, data):
        """Write data to the LCD.

        It is expected that a derived HAL class will implement this
        function.
        """
        raise NotImplementedError

    def hal_sleep_us(self, usecs):
        """Sleep for some time (given in microseconds)."""
        time.sleep_us(usecs)

```
## lcd01.py
```
from esp8266_i2c_lcd import I2cLcd
from machine import I2C,Pin

# GPIO 12-D6,GPIO 13-D7
i2c = I2C(scl=Pin(13), sda=Pin(12), freq=100000)
lcd = I2cLcd(i2c, 0x27, 2, 16)
lcd.clear()

lcd.move_to(0, 0)  #(0,0) 位置
lcd.putstr("Hello World!") 
```
## lcd02.py
```
from esp8266_i2c_lcd import I2cLcd
from machine import I2C,Pin

# GPIO 12-D6,GPIO 13-D7
i2c = I2C(scl=Pin(13), sda=Pin(12), freq=100000)
lcd = I2cLcd(i2c, 0x27, 2, 16)
lcd.clear()

lcd.move_to(2, 0)  #(0,2) 位置
lcd.putstr("R=100")
lcd.putchar(chr(0xF4)) #Ω

lcd.move_to(2, 1)  #(1,2) 位置
lcd.putstr("T=25") 
lcd.putchar(chr(0xDF)) #°
lcd.putchar("C") #C
```
## main.py
```
from esp8266_i2c_lcd import I2cLcd
from machine import I2C,Pin,ADC
from time import sleep

# GPIO 12-D6,GPIO 13-D7
DEFAULT_I2C_ADDR = 0x27 # 位址
A0 = ADC(0) # 讀取 A0 埠

i2c = I2C(scl=Pin(13), sda=Pin(12), freq=100000)
lcd = I2cLcd(i2c, DEFAULT_I2C_ADDR, 2, 16)
lcd.clear()

while True:
  A0_value = A0.read() #讀取A0埠
  print(A0_value)      #顯示轉換後的數值  

  lcd.move_to(0, 0)    #(0,0) 位置
  lcd.putstr("A0=" + str(A0_value)  + "   ") 
  sleep(0.5)
```
# ch32
---
## Socket
---
### Client.py
```
import socket
s = socket.socket()
s.connect(('localhost', 6688))
while True:
    msg = input('請輸入訊息：')
    s.send(msg.encode('utf8'))
    reply = s.recv(128) #最多可接收128個字元
    
    if reply == b'exit':
        print('關閉連線')
        s.close()
        break
    print("收到 server 回傳訊息：" + reply.decode('utf8'))
```
### Server.py
```
import socket
HOST = 'localhost'
PORT = 6688
s = socket.socket()
s.bind((HOST, PORT))
s.listen(5) #監聽客戶端的連線請求
print('{} 伺服器在 {} 埠建立！'.format(HOST, PORT))
client, addr = s.accept() #接受客戶端的連線
print('客戶端位址：{}，埠號：{}'.format(addr[0], addr[1]))

while True:
    msg = client.recv(128).decode('utf8')
    print ('收到 client 訊息：' + msg)
    reply = '已讀不回'

    if msg == 'Hello':
        reply = '大家好!'
    elif msg == 'bye':
        client.send(b'exit')
        break

    client.send(reply.encode('utf8'))

client.close()
```
---
## boot.py
```
# This file is executed on every boot (including wake-boot from deepsleep)
#import esp
#esp.osdebug(None)
import uos, machine
#uos.dupterm(None, 1) # disable REPL on UART(0)
import gc

# 連線基地台
SSID='自已的SSID'
PASSWORD='自已的密碼'
def do_connect():
    sta = network.WLAN(network.STA_IF) # Station
    if not sta.isconnected():
        print('正在連線中...')
        sta.active(True) #啟用 STA 模式
        sta.connect(SSID, PASSWORD) #連線基地台
        # 等侯連線
        while not sta.isconnected():
            pass
    print('連線成功!')
    #print(sta.ifconfig()) # 顯示網址、網路遮罩、閘道器和 DNS

#import webrepl
#webrepl.start()
gc.collect()
```
## eHappy.py
```
import urequests
import network
import time

SSID='自己的SSID'
PASSWORD='自己的密碼'
def do_connect():
    sta = network.WLAN(network.STA_IF) # Station
    if not sta.isconnected():
        print('正在連線中...')
        sta.active(True) #啟用 STA 模式
        sta.connect(SSID, PASSWORD) #連線基地台
        # 等侯連線
        while not sta.isconnected():
            pass
    print('連線成功!')
    #print(sta.ifconfig()) # 顯示網址、網路遮罩、閘道器和 DNS
              
do_connect() # 連線基地台
r=urequests.get("http://www.e-happy.com.tw")
r.encoding='utf-8'
time.sleep(3)
print("下載完畢!")
if (r.status_code==200):
    print(r.raw.read(100))

```
## http_request.py
```
import network
import socket

SSID='自己的SSID'
PASSWORD='自己的密碼'
def do_connect():
    sta = network.WLAN(network.STA_IF) # Station
    if not sta.isconnected():
        print('正在連線中...')
        sta.active(True) #啟用 STA 模式
        sta.connect(SSID, PASSWORD) #連線基地台
        # 等侯連線
        while not sta.isconnected():
            pass
    print('連線成功!')
              
do_connect() # 連線基地台

httpRequest = b'''\
GET /{path} HTTP/1.1
Host:{host}
User-Agent: D1-mini

'''

url = 'http://micropython.org/ks/test.html'
_, _, host, path = url.split('/', 3)
addr = socket.getaddrinfo(host, 80)[0][-1]
s = socket.socket()
s.connect(addr)
s.send(httpRequest.format(path=path, host=host))

while True:
    data = s.recv(128) #接收訊息
    if data:
        print(data.decode('utf8'), end='')
    else:
        break

s.close()
```
## https_request.py
```
import network
import socket
import ussl

SSID='自己的SSID'
PASSWORD='自己的密碼'
def do_connect():
    sta = network.WLAN(network.STA_IF) # Station
    if not sta.isconnected():
        print('正在連線中...')
        sta.active(True) #啟用 STA 模式
        sta.connect(SSID, PASSWORD) #連線基地台
        # 等侯連線
        while not sta.isconnected():
            pass
    print('連線成功!')
              
do_connect() # Connect to network

httpRequest = b'''\
GET /{path} HTTP/1.0
Host:{host}
User-Agent: D1-mini

'''

url = 'https://micropython.org/ks/test.html'
_, _, host, path = url.split('/', 3)
addr = socket.getaddrinfo(host, 443)[0][-1] #埠號 443
s = socket.socket()
s.connect(addr)
s = ussl.wrap_socket(s) #加密
s.write(httpRequest.format(path=path, host=host)) #傳送加密訊息

while True:
    data = s.read(128) #接收訊息
    if data:
        print(data.decode('utf8'), end='')
    else:
        break
s.close()
```
## main.py
```
import urequests # 不可使用 requests
import time

r=urequests.get("http://www.e-happy.com.tw")
r.encoding='utf-8'
time.sleep(3)
print("下載完畢!")
if (r.status_code==200):
    print(r.raw.read(100))


```
## Station.py
```
import network

SSID='自己的SSID'
PASSWORD='自己的密碼'
sta = network.WLAN(network.STA_IF)

if not sta.isconnected():
    print('正在連線中...')
    sta.active(True) #啟用 STA 模式
    sta.connect(SSID, PASSWORD) #連線基地台
    # 等侯連線
    while not sta.isconnected():
        pass
print('連線成功!')
print(sta.ifconfig()) # 顯示網址、網路遮罩、閘道器和 DNS
```
# ch33
---
## esp8266_ThingSpeak
---
### Read_ThingSpeak.py
```
import urequests as req
import network
import json

SSID='自己的SSID'
PASSWORD='自己的密碼'
def do_connect():
    sta = network.WLAN(network.STA_IF) # Station
    if not sta.isconnected():
        print('正在連線中...')
        sta.active(True) #啟用 STA 模式
        sta.connect(SSID, PASSWORD) #連線基地台
        # 等侯連線
        while not sta.isconnected():
            pass
    print('連線成功!')
              
do_connect() # Connect to network

host='https://api.thingspeak.com'       
api_key='L2GT60TEPN8MGMOO'   # Read Key (光線感測器)
ChannelID='923788'
records=3 # 讀取最後 3 筆
  
apiURL='%s/channels/%s/feeds.json?api_key=%s&results=%d' %(host,ChannelID, api_key,records) 
print(apiURL)

r = req.get(apiURL)
if r.status_code == 200:
    print('最後 3 筆資料讀取成功!')
    print(r.text)
    
    jsondata = json.loads(r.text)    
    data= jsondata["feeds"]
    print("\n",data)
else:
    print('資料讀取錯誤!')
    


```
### ThingSpeak.py
```
from machine import ADC
import urequests as req
import network,time

SSID='自己的SSID'
PASSWORD='自己的密碼'
def do_connect():
    sta = network.WLAN(network.STA_IF) # Station
    if not sta.isconnected():
        print('正在連線中...')
        sta.active(True) #啟用 STA 模式
        sta.connect(SSID, PASSWORD) #連線基地台
        # 等侯連線
        while not sta.isconnected():
            pass
    print('連線成功!')
              
do_connect() # Connect to network

A0 = ADC(0)

host='https://api.thingspeak.com'       
api_key='0O6HE9KF3DR1W1DV'   # Write Key (光線感測器)

def sendData():    
    try:    
        value = A0.read() # 讀取 A0 埠
    except OSError as e:
        print(e)
        return
  
    apiURL='%s/update?api_key=%s&field1=%s' %(host, api_key, value) 
    print(apiURL)

    r = req.get(apiURL)
    if r.status_code == 200:
        print('第 {} 筆資料傳送成功!' .format(r.text))
    else:
        print('資料傳送錯誤!')  

try:
    while True:
        sendData()
        time.sleep(20)        
except:
    print('結束執行')
```
---
===





