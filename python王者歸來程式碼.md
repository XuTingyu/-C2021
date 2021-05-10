
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













































