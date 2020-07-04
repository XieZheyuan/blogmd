---
title: python 猿编程模块（一）ybc_speech
tags: [计算机, python, 猿编程]
date: 2019/10/06
description: 猿编程模块 ybc_speech
---

首先先安装模块

```bash
C:\Python36\python.exe -m pip install ybc-speech
```
**record**:录制音频
```python
def record(filename, seconds=__SECONDS, to_dir=__TO_DIR, rate=__RATE, channels=__CHANNELS, chunk=__CHANNELS):
    """
    功能：录制音频文件。

    参数 filename 是录制生成的语音文件的名字，

    可选参数 seconds 是录制时长（单位：秒），默认 5 秒，

    可选参数 to_dir 是存放语音文件的目录，默认为当前目录，

    可选参数 rate 是录制采样率，1 代表 16000，0 代表 8000，默认为 1，

    可选参数 channels 是声道，默认 1，

    可选参数 chunk 是一次读取的字节数，默认 1024，

    返回：录制的音频文件的路径。
    """
```

##### 示例：

```python
import ybc_speech as s
import os
s.record("aaa.wav",10)
os.system("aaa.wav")
```
**voice2text**:语音转文字

```python
def voice2text(filename='', rate=__RATE, format_type=__FORMAT_TYPE):
    """
    功能：把语音文件转换成文字。

    参数 filename 是当前目录下期望转换成文字的语音文件的名字，

    可选参数 rate 是语音文件的采样率，1 代表 16000，0 代表 8000，默认为 1，

    可选参数 format_type 是语音文件的类型，默认 PCM 格式，

    返回：转换成的文字。
    """
```
##### 示例：

```python
import ybc_speech as s
#import os
print(s.voice2text("aaa.wav"))
```
**text2voice**:语音合成

```python
def text2voice(text, filename, speaker=__SPEAKER, speed=__SPEED, aht=__AHT, apc=__APC, volume=__VOLUME, _format=__FORMAT, rate=__RATE):
    """
    功能：把文字转换成语音。

    参数 text 是待转换的文字，

    参数 filename 是生成的语音文件的名字，

    可选参数 speaker 是发音人，1 代表小刚（男声），2 代表小云（女声），默认为1，

    可选参数 speed 是语速，1 代表正常速度，0.5 代表慢速，2 代表快速，默认为1，

    可选参数 aht 是音高，默认为 0，

    可选参数 apc 是音色，默认为 58，

    可选参数 volume 是音量，默认为 100，

    可选参数 _format 是语音文件的格式，1 代表 PCM，2 代表 WAV，3代表 MP3，默认为 2 ，

    可选参数 rate 是语音采样率，1 代表 16000，0 代表 8000，默认为 1，

    返回：生成的语音文件的名字。
    """
```
##### 示例：

```python
import ybc_speech as s
import os
s.text2voice("Hello","hello.wav",2)
os.system("hello.wav")
```
**speak**:播放便捷函数

```python
def speak(text='', speaker=__SPEAKER, speed=__SPEED, aht=__AHT, apc=__APC):
    """
    功能：朗读一段文字。

    参数 text 是待朗读的文字，

    可选参数 speaker 是发音人，1 代表小刚（男声），2 代表小云（女声），默认为1，

    可选参数 speed 是语速，1 代表正常速度，0.5 代表慢速，2 代表快速，默认为1，

    可选参数 aht 是音高，默认为 0，

    可选参数 apc 是音色，默认为 58，

    返回：无。
    """
```
**常量表**

```python
__RATE = 16000
__FORMAT_TYPE = 2
__SECONDS = 5
__TO_DIR = None
__CHANNELS = 1
__CHUNK = 1024
__SPEAKER = 1
__SPEED = 1
__AHT = 0
__APC = 58
__VOLUME = 100
__FORMAT = 2


```
首发于CSDN博客https://blog.csdn.net/pythonbilly
