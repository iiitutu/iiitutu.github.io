# 第一章 - 数据结构和算法

## 1.1 将序列分解为单独的变量

```python
# 变量数量与结构要与列表相吻合
# 只要对象是iterable，就可以使用unpack操作
data = ['ACME', 50, 91.1, (2012, 12, 21)]
name, _, price, date = data  # 使用下划线这类变量名，即约定这个变量是想要丢弃的

print(name, price, date)  # ACME 91.1 (2012, 12, 21)
```

```python
# 如果数量不匹配，将得到ValueError
p = (4, 5)
x, y, z = p

# ValueError: not enough values to unpack (expected 3, got 2)
```

## 1.2 从任意长度的可迭代对象中分解元素

```python
user_record = [
    'Dave', 'dave@example.com', '13311122332', '15821203400', '50922234'
]
name, email, *phone_numbers = user_record

print(name, email)  # Dave dave@example.com
print(phone_numbers)  # ['13311122332', '15821203400', '50922234']
```

```python
records = [
    {'foo', 1, 2},
    {'bar', 'hello'},
    {'foo', 3, 4},
]

for tag, *args in records:
    if tag == 'foo':
        print(args)
    else:
        print('bar', args)
"""
[2, 1]
bar ['bar']
[3, 4]
"""

```