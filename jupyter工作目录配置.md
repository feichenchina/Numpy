[TOC]



# 下载jupyter，安装完毕





## 配置jupyter工作目录

首先在命令行窗口进入jupyter的安装目录，运行命令 jupyter notebook --**generate**-config

此时会生成  Jupyter_notebook_config.py 文件

在文件中找到     c.NotebookApp.notebook_dir    ，后面写入自己的路径

例子展示   

```c.NotebookApp.notebook_dir = 'E:\code1\Jupyter'```

或者直接在文件最后加入这句话也可以



## 配置jupyter浏览器

找到c.NotebookApp.browser = ''，在下方输入

import webbrowser

webbrowser.register("chrome",None,webbrowser.GenericBrowser(u"C:\\ProgramFiles(x86)\\Google\\Chrome\\Application\\chrome.exe"))

c.NotebookApp.browser = 'chrome'