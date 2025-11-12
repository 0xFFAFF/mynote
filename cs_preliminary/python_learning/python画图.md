# python 绘图教程

## 安装依赖库
执行命令`pip install matplotlib`

## 简单绘图命令

```python
import matplotlib as plt # 导入相关库

x = [1,2,3,4]
y = [1,2,3,4]

# 画图
plt.plot(x,y)
plt.xlabel('这是x轴') # 设置x轴标题
plt.ylabel('这是y轴') # 设置y轴标题
plt.title('设置图的标题') # 设置图的标题
plt.show() # 把图片展示出来
```

## 稍微进阶一点
在这个例子里，我们要**绘制多组数据**，为每组数据设置不同的**线条粗细，颜色，图例**，展示**标题和图例**
```python
import matplotlib as plt # 导入相关库
x_1 = [1,2,3,4]
y_1 = [1,2,3,4]

x_2 = [1,2,3,4]
y_2 = [1,4,9,16]

plt.figure(figsize(10,6)) # 设置图片的大小
plt.plot(x_1, y_1, linewidth = 2.5, color = 'red', linestyle = '-', marker = 'o',
        markersize = 8, label = '线性函数')
"""
plt.plot(x_1, y_1, linewidth = 2.5, color = 'red', linestyle = '-', marker = 'o',
        markersize = 8, label = '线性函数')
x_1, y_1是要绘图的数据;
linewidth设置画出来的线条的粗细；
color设置画出来的线条的颜色；
linestyle设置画出来线条的样子，是实线啊还是虚线呀；
marker是设置绘图标记点的形状；
markersize是设置绘图标记点的大小
label是设置图例
"""
plt.plot(x_2, y_2, lw=2, c='blue', ls='--', marker='s', 
         markersize=6, label='二次函数')

# 接下来设置标题和标签
plt.title('多组数据对比图'， fontsize = 16)
plt.xlabel('x轴', fontsize = 10)
plt.ylabel('y轴', fontsize = 10)

# 接下来我们设置一下刻度
plt.xticks([0, 1, 2, 3, 4, 5])
plt.yticks([0, 1, 4, 9, 16, 25])

# 设置一下刻度的范围
plt.xlim(-0.5, 0.5)
plt.ylin(-2, 27)

# 设置网格
plt.grid(True, alpha = 0.3) # True为显示网格， alpha是设置网格的透明度

# 设置图例以及图例的位置
plt.legend(loc='upper left')
```

:star:常用颜色和线型
```python
# 颜色可以用：
# - 单字母: 'r', 'g', 'b', 'c', 'm', 'y', 'k', 'w'
# - 英文名: 'red', 'green', 'blue', 'orange', 'purple'
# - 十六进制: '#FF5733'
# - RGB元组: (0.1, 0.2, 0.5)

# 线型可以用：
# '-'   实线
# '--'  虚线
# '-.'  点划线
# ':'   点线

# 标记可以用：
# 'o'   圆圈
# 's'   正方形
# '^'   三角形
# '*'   星号
# '+'   加号
# 'x'   叉号
```

## 更加进阶一点
现在我们想在一张画布上多张图
```python
import matplotlib as plt # 导入相关库
fig, axes = plt.subplots(2, 2, figsize=(10,8))
axes[0,0].plot()
axes[0,0].set_title('这是第一张图')

axes[0,1].plot()
axes[0,0].set_title('这是第二张图')

axes[1,0].plot()
axes[0,0].set_title('这是第三张图')

axes[1,1].plot()
axes[0,0].set_title('这是第四张图')

plt.tight_layout() # 自动调整子图间距，防止标题、标签重叠
fig.suptitle('这是总标题', fontsize = 16)
```