title: python简易数据分析
tags:
  - 计算机
  - 数学
  - python
  - 数据分析
description: 简易数据分析
date: 2020-07-04 18:47:50
---

#  python简易数据分析
## 1、平均数(Average)
话不多说，直接上代码
```python
def average(data):
    sum_ = sum(data) # 调用内置求和函数
    a_val = sum_ / len(data)
    return a_val
```

## 2、方差(Variance)
### 何谓方差?
> 方差是在概率论和统计方差衡量随机变量或一组数据时离散程度的度量。概率论中方差用来度量随机变量和其数学期望（即均值）之间的偏离程度。统计中的方差（样本方差）是每个样本值与全体样本值的平均数之差的平方值的平均数。在许多实际问题中，研究方差即偏离程度有着重要意义。
>—— [百度百科](https://baike.baidu.com/item/%E6%96%B9%E5%B7%AE/3108412)

![方差公式图片](/blogimages/variance.svg)
### 代码
```python
def variance(data):
    a_val = average(data)
    var = 0
    for i in data:
        var += abs(a_val - i) ** 2
    
    var /= len(data)
    return a_val
```

## 平均差(Mean Deviation)
### 何谓平均差
> 平均差（Mean Deviation）是表示各个变量值之间差异程度的数值之一。指各个变量值同平均数的离差绝对值的算术平均数。
  平均差异大，表明各标志值与算术平均数的差异程度越大，该算术平均数的代表性就越小；平均差越小，表明各标志值与算术平均数的差异程度越小，该算术平均数的代表性就越大。因离差和为零，离差的平均数不能将离差和除以离差的个数求得，而必须将离差取绝对数来消除正负号。平均差是反应各标志值与算术平均数之间的平均差异。
>——[百度百科](https://baike.baidu.com/item/%E5%B9%B3%E5%9D%87%E5%B7%AE)

![平均差公式图片](/blogimages/mean.svg)
## 代码

```python
def mean(data):
    a_val = average(data)
    var = 0
    for i in data:
        var += abs(a_val - i)

    var /= len(data)
    return var
```

## 标准差(Standard Deviation)

### 何谓标准差
> 标准差（Standard Deviation） ，是离均差平方的算术平均数的平方根，用σ表示。在概率统计中最常使用作为统计分布程度上的测量。标准差是方差的算术平方根。标准差能反映一个数据集的离散程度。平均数相同的两组数据，标准差未必相同。
> ——[百度百科](https://baike.baidu.com/item/%E6%A0%87%E5%87%86%E5%B7%AE)

### 代码
```python
from math import sqrt

def sd(data):
    v = sqrt(variance(data))
    return v
```

## 极差(Range)
这就更不用说啦！
```python
def range_(data):
    max_ = max(data)
    min_ = min(data)
    return max_ - min_
```

## 完整代码
完整代码如下所示（PEP通过）
```python
from math import sqrt


def average(data):
    sum_ = sum(data)
    a_val = sum_ / len(data)
    return a_val


def variance(data):
    a_val = average(data)
    var = 0
    for i in data:
        var += abs(a_val - i) ** 2

    var /= len(data)
    return a_val


def mean(data):
    a_val = average(data)
    var = 0
    for i in data:
        var += abs(a_val - i)

    var /= len(data)
    return var


def sd(data):
    v = sqrt(variance(data))
    return v


def range_(data):
    max_ = max(data)
    min_ = min(data)
    return max_ - min_

```