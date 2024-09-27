# Python-Embed-Win64

- 添加了 **pip** 和 **tkinter** 的 Embedding Python

## 配置环境

修改 **python\*._pth** 文件
```shell
cat .\python*._pth

python311.zip
packages
.

# Uncomment to run site.main() automatically
import site
```

也可以通过指定 **PYTHONPATH** 环境变量来移除 **python\*._pth** 文件
```shell
# cd 到 python.exe 所在目录, 或者使用绝对路径
# 如果需要写入到系统环境变量, 一定要使用绝对路径
$Env:PYTHONPATH = ".\packages;.\Lib\site-packages"
```

*大多数的时候单项目修改 **python\*._pth** 文件即可。*
*不使用 **python\*._pth** 是为了解决工作目录的问题，也就是你在外部调用 **python** 时会出现找不到模块的问题。*

## 运行 Python

**pip** 模块
```shell
.\python.exe -m pip list

Package    Version
---------- -------
pip        24.0
setuptools 65.5.0

[notice] A new release of pip is available: 24.0 -> 24.2
[notice] To update, run: python.exe -m pip install --upgrade pip
```

**tkinter** 模块
```shell
.\python.exe
Python 3.11.10 (tags/v3.11.10:0c47759, Sep 27 2024, 21:18:53) [MSC v.1941 64 bit (AMD64)] on win32
>>> import tkinter as tk
>>> tk.TkVersion
8.6
```
