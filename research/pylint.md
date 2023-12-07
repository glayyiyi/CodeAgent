实现解析Python代码模块间调用关系，有以下几个步骤：

- 首先，需要安装一个Python扩展库，叫做pylint，它可以分析Python程序中函数之间的调用关系，并生成一个图形文件。
- 然后，需要安装一个软件，叫做graphviz，它可以根据图形文件绘制出调用关系图，支持多种格式，如png，svg，pdf等。
- 接着，需要在XAgent项目下进行调用关系图的生成：


```python
pip install pylint
sudo apt install graphviz
pip install pylint-plugin-utils
pip install pylint-json2html
cd XAgent/XAgent
pyreverse XAgent
dot -Tpng classes.dot -o my.png    
```

- 最后，就会在当前目录下生成一个名为my.png的文件，它就是调用关系图。可以用任意图片查看器打开它
  
![调用关系效果图](./packages.png)

  
