# python dict操作
```python
# 创建字典
my_dict = {
    'name': 'Alice',
    'age': 25,
    'city': 'New York'
}

# 访问字典元素
print(my_dict['name'])  # 输出: Alice
print(my_dict['age'])   # 输出: 25

# 添加或修改元素
my_dict['age'] = 26  # 修改age
my_dict['job'] = 'Engineer'  # 添加job

# 删除元素
del my_dict['city']  # 删除city
my_dict.pop('job')  # 删除job并返回其值

# 获取所有keys
keys = my_dict.keys()
# 获取所有values
values = my_dict.values()
# 获取所有key-value对
items = my_dict.items()

# 遍历字典
for key, value in my_dict.items():
    print(f"{key}: {value}")

```