# python中numpy库的使用


```python
vector1 = np.array([1, 2, 3])   #一个向量的初始化
vector2 = np.array([4, 5, 6])
np.mean(vector1)                #获取向量的均值
np.var(vector1)                 #向量的方差
np.dot(vector1, vector2)        #两个向量的内积
np.cov(vector1, vector2)        #生成两个向量的协方差矩阵
```