# 第一章 - 数据结构和算法

## 1.1 将序列分解为单独的变量

```python
# unpack tuple
p = (4, 5)
x, y = p

print(x, y)  # 4, 5
```

```python
# 变量数量与结构要与列表相吻合
data = ['ACME', 50, 91.1, (2012, 12, 21)]
name, shares, price, date = data

print(name, shares, price, date)  # 'ACME', 50, 91.1, (2012, 12, 21)
```

```python
# 如果数量不匹配，将得到ValueError
p = (4, 5)
x, y, z = p

# ValueError: need more than 2 values to unpack
```

```python
# 只要对象是iterable，就可以使用unpack操作
s = 'Hello'
a, _, c, _, e = s  # 使用下划线这类变量名，即约定这个变量是想要丢弃的

print(a,c,e)  # H, l, o
```

