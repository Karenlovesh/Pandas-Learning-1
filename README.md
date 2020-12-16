# Pandas-Learning-1


L=[]
def my_func(x): ## def 定义函数
    return 2*x 
for i in range(5):
    L.append(my_func(i)) ## L.append（）运行函数，且赋值至L
L

[0, 2, 4, 6, 8]

[my_func(i) for i in range(5)] ## range(N)默认0-（N-1）;range(a,b)默认a-（b-1）

[0, 2, 4, 6, 8]

[my_func(i) for i in range(3,7)] 

[6, 8, 10, 12]

[m+'_'+n for m in ['3','7'] for n in ['4','8']]

['3_4', '3_8', '7_4', '7_8']

value='cat' if 2>1 else 'dog'

value

'cat'

#自编练习，但似乎不对

def my_func(x):
    return 2*x
def my_func1(x):
    return x*x
A=[]
for i in range(5):
    A.append(my_func(i))
B=[]
for i in range(5):
    B.append(my_func1(i))

B

[0, 1, 4, 9, 16]

C=dict(zip(A,B))

value='cat' if i>j else 'dog' ,for i in C

  File "<ipython-input-93-79651631e311>", line 1
    value='cat' if i>j else 'dog' ,for i in C
                                   ^
SyntaxError: invalid syntax

##分割线

my_func=lambda x:2*x ## lambda匿名函数
multi_para_func=lambda a,b:a+b
multi_para_func(2,3)

5

[(lambda x:x*x) (i) for i in range (1,6)]

[1, 4, 9, 16, 25]

list(map(lambda x: x*3,range(1,6))) ## map函数

[3, 6, 9, 12, 15]

list(map(lambda x,y:str(x)+'_'+y,range(3,6),list('abc')))

['3_a', '4_b', '5_c']

L1,L2,L3=list('abc'),list('def'),list('ghi') ## list 定义数组元素
list(zip(L1,L2,L3))
tuple(zip(L1,L2,L3)) ## tuple 及 zip两种写法等同

(('a', 'd', 'g'), ('b', 'e', 'h'), ('c', 'f', 'i'))

for i,j,k in zip(L1,L2,L3):
    print(i,j,k)

a d g
b e h
c f i

for index,value in  enumerate(L1):
    print(index,value)

0 a
1 b
2 c

dict(zip(L1,L2)) ## dict 建立映射

{'a': 'd', 'b': 'e', 'c': 'f'}

#numpy分割线

import numpy as np

np.array([1,2,3])

array([1, 2, 3])

A=np.linspace(1,5,11) ##np.linspace 构建等差数列:起始、终止（包括），样本总数
B=np.arange(1,7,2)  ## np.arrange 构建等差数列：起始、终止（不包括），步长

A,B

(array([1. , 1.4, 1.8, 2.2, 2.6, 3. , 3.4, 3.8, 4.2, 4.6, 5. ]),
 array([1, 3, 5]))

 np.random.rand(3) ##随机数组

my_list = ['a', 'b', 'c', 'd']

np.random.choice(my_list, 2, replace=False, p=[0.1, 0.7, 0.1 ,0.1])
array(['b', 'd'], dtype='<U1')

 np.random.choice(my_list, (3,3)) #抽样

martix_target =  np.arange(4).reshape(-1,2)
martix_target
np.linalg.norm(martix_target, 'fro')
np.linalg.norm(martix_target, np.inf)
np.linalg.norm(martix_target, 2) ##向量范数，矩阵范数

 

