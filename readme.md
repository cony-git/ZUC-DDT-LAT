# ZUC S盒 的DDT LAT表
---
##  ZUC S0和S1的差分分析表和线性分析表的实现,代码

如代码DDT.py LAT.py

---
## 实验结果
如文件DDTTABLE.txt LATTABLE.txt

---
## 设计思路
DDT表
每一行为delta x,每一列为delta y
对于每一个delta x，遍历S盒得到的x,y映射表，求得x1,x2,y1,y2,delta y
对于每一个delta x,求得对应delta y 的个数
得到DDT表

LAT表
每一行为ai&xi,每一列为bi&yi
根据S盒得到x,y的映射表
对于每一个sum(ai&xi)^sum(bi&yi)==0进行计数
得到LAT表

---
## why final key mixing?
因为S盒可逆，如果不在最后一轮添加一个秘钥混淆，最后一轮S盒相当于没有。故需要在最后加上一轮key mixing.
