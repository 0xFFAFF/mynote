# 数据读取
读取csv数据，用于画图
```python
import pandas as pd #导入相关库
from pathlib import Path 

df = pd.read_csv('data.csv') # 读取数据

# 获取文件夹下的所有文件
directory = Path('data')
# 只获取文件(排除文件夹)
for item in directory.iterdir():
    if item.is_file():
        print(item)
```


pandas数据读取
```python
import pandas as pd
#跳过开头行
df = pd.read_csv('data.csv'， skiprows = 3) # 读取csv数据
#跳过末尾行
df = pd.read_csv('data.csv'， skipfooter = 2, engine='python') # 读取csv数据
#跳过开头行并读取特定的列数
df = pd.read_csv('data.csv'， skiprows = 3, nrows=5) # 读取csv数据

# 数据选择
data = df['col1'] # 选择单列，生成Series
data = df[['col1', 'col2']] # 选择特定的列，生成新的DataFrame
data = df.iloc[0:5, 0:2] # 通过行列索引选择数据
data = df.loc[0:5, ['col1', 'col2']] # 通过标签选择数据

# 数据变成dataframe

# 方法1：字典的值是列表（每个key是列名）
data = {
    'name': ['Alice', 'Bob', 'Charlie'],
    'age': [25, 30, 35],
    'city': ['Beijing', 'Shanghai', 'Guangzhou']
}
# 方法2：字典列表（每个字典是一行）
data = [
    {'name': 'Alice', 'age': 25, 'city': 'Beijing'},
    {'name': 'Bob', 'age': 30, 'city': 'Shanghai'},
    {'name': 'Charlie', 'age': 35}  # 缺失值会自动填充NaN
]
# 一维列表转成单列DataFrame
data = [1, 2, 3, 4, 5]
df = pd.DataFrame(data, columns=['numbers'])

df = pd.DataFrame(data)
df.to_csv('output.csv', index=False) # 保存为csv文件
```