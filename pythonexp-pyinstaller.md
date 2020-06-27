---
title: Python经验帖——pyinstaller
tags: [计算机, python,pyinstaller]
---

# PyInstaller介绍

PyInstaller是一个简单的python编译程序，可以把** py ** 源文件编译成 ** exe ** 可执行文件（据说还可以变成.app等，但没有亲测过）

# PyInstaller安装

直接运行pip命令即可

```powershell
python -m pip install pyinstaller //Windows/MS-DOS
pip install pyinstaller //Liunx/Unix
pip3 install pyinstaller //Mac
```

> 注：如果下载过慢或超时(Timeout)那么可以选择清华镜像，详细参考 [让python pip使用国内镜像(Cnblog)](https://www.cnblogs.com/wqpkita/p/7248525.html)


# PyInstaller使用

## 写一个python程序

1.py
```python
print("Hello World")
```
**strong text**
## 尝试编译
```powershell
python -m PyInstaller 1.py
```
会生成dist目录，dist目录下有1目录，里面就是所有文件

## 其他

### -w

生成GUI程序（无CMD窗口）

### -F

生成单个文件

### -i [ico]

加图标（很有用）
