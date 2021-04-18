

```python
import numpy as np
array=np.array([2,4,8,16])#通过np.array()方法创建一个名为array的array类型，参数是一个list
array
```




    array([ 2,  4,  8, 16])




```python
array.max()#array中最大数
```




    16




```python
array.min()#array中最小数
```




    2




```python
array*2#array中所有数乘2
```




    array([ 4,  8, 16, 32])




```python
array**2#array中所有数的平方
```




    array([  4,  16,  64, 256], dtype=int32)




```python
array+1#array中所有数+1
```




    array([ 3,  5,  9, 17])




```python
array/2#array中所有数除2
```




    array([1., 2., 4., 8.])




```python
array%2#array中所有数取余
```




    array([0, 0, 0, 0], dtype=int32)




```python
array.argmax()#获得该组数据中元素值最大的那个数据的索引，下标从0开始
```




    3




```python
#Numopy高维数据处理
import numpy as np
array_1=np.array([[1,2],[3,4],[5,6]])
#创建一个二维数组，用来表示一个3行2列的矩阵，名为array
array_1
```




    array([[1, 2],
           [3, 4],
           [5, 6]])




```python
array_1.shape#查看矩阵维度
```




    (3, 2)




```python
array_1.argmax()
```




    5




```python
array_1.flatten()#将3行2列矩阵转换乘一行表示
```




    array([1, 2, 3, 4, 5, 6])




```python
array_1.reshape(2,3)将维度为3*2，转换成2*3的形式
```




    array([[1, 2, 3],
           [4, 5, 6]])




```python
array_1.size#查看矩阵元素数量
```




    6




```python
#Nupmy创建特殊array类型
import numpy as np
array_zeros=np.zeros((2,3,3))#创建一个维度为（2，3，3）的0矩阵
array_zeros
```




    array([[[0., 0., 0.],
            [0., 0., 0.],
            [0., 0., 0.]],
    
           [[0., 0., 0.],
            [0., 0., 0.],
            [0., 0., 0.]]])




```python
array_ones=np.ones((2,3,3))#创建一个维度为（2，3，3）全为1的矩阵
array_ones
```




    array([[[1., 1., 1.],
            [1., 1., 1.],
            [1., 1., 1.]],
    
           [[1., 1., 1.],
            [1., 1., 1.],
            [1., 1., 1.]]])




```python
array_ones.shape
```




    (2, 3, 3)




```python
array_arange=np.arange(10)#生成一个array，从0递增到10，步长为1
array_arange
```




    array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])




```python
array_linspace=np.linspace(0,10,5)#生成一个array，从0递增到10，步长为5
array_linspace
```




    array([ 0. ,  2.5,  5. ,  7.5, 10. ])




```python
#Numpy基本计算
import numpy as np
np.abs([1,-1,-2,3,4])#abs：取绝对值
```




    array([1, 1, 2, 3, 4])




```python
np.sin(np.pi/2)#求pi/2的正弦值
```




    1.0




```python
np.arctan(1)#求反正切值
```




    0.7853981633974483




```python
np.exp(2)#求自然常数e的平方
```




    7.38905609893065




```python
np.power(2,3)#2的3次方
```




    8




```python
np.dot([1,2],[3,4])#将两个向量点积1*3+2*4
```




    11




```python
np.sqrt(16)#对16开方
```




    4.0




```python
np.sum([1,2,3,4,5,6,7,8,9,10])#求和
```




    55




```python
np.mean([1,2,3,4])
```




    2.5




```python
np.std([1,2,3,4])#求标准差
```




    1.118033988749895




```python
#Numpy的线性代数操作
import numpy as np
#定义a,b两个向量
a=np.array([1,2,3])
b=np.array([2,3,4])
np.dot(a,b)#向量点积1*2+2*3+3*4=20
```




    20




```python
a.dot(b)##向量点积1*2+2*3+3*4=20
```




    20




```python
np.dot(a,b.T)#将行向量a与列向量b.T相乘（相当于求两个行向量的点积）
#dot()方法：默认两个向量点积，对于符合叉乘格式的矩阵，自动进行叉乘。
```




    20




```python
matrix_a=np.array([[1,2],
                   [3,4]])
matrix_b=np.dot(matrix_a,matrix_a.T)
matrix_b
```




    array([[ 5, 11],
           [11, 25]])




```python
np.linalg.norm([1,2])#求一个向量范数的值
#norm()没有指定第2个参数，则默认为求2范数
```




    2.23606797749979




```python
np.linalg.norm([1,-2],1)#求1范数
#1范数的结果为向量中各元素绝对值之和，结果为3.0
```




    3.0




```python
np.linalg.norm([1,2,3,4],np.inf)#求向量的无穷范数，np.inf代表正无穷，也就是元素值中最大的那个即：4.0
```




    4.0




```python
np.linalg.norm([1,2,3,4],-np.inf)#求向量的负无穷范数，np.inf代表正无穷，也就是元素值中最小的那个即：1.0
```




    1.0




```python
np.linalg.norm(matrix_b)
#除了向量可以求范数，矩阵也可以有类似的运算，即为F范数
```




    29.866369046136157




```python
#求矩阵的行列式
np.linalg.det(matrix_a)
```




    -2.0000000000000004




```python
np.trace(matrix_a)#求矩阵的迹
```




    5




```python
np.linalg.matrix_rank(matrix_a)#求矩阵的秩
```




    2




```python
a*b#将两个向量中的元素分别相乘
```




    array([ 2,  6, 12])




```python
a**b#相当于a的b次方
```




    array([ 1,  8, 81], dtype=int32)




```python
np.linalg.pinv(matrix_a)#求矩阵逆矩阵，pinv()求的是伪逆矩阵，inv()是逆矩阵
```




    array([[-2. ,  1. ],
           [ 1.5, -0.5]])




```python
np.linalg.inv(matrix_a)
```




    array([[-2. ,  1. ],
           [ 1.5, -0.5]])




```python

```
