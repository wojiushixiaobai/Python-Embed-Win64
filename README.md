# Python-Embed-Win64

- 添加了 **pip** 和 **tkinter** 的 Embedding Python

配置环境
```shell
cat .\python*._pth

python311.zip
packages
.

# Uncomment to run site.main() automatically
import site
```

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