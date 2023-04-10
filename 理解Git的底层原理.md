# 理解Git的底层原理

2023年4月10日

参考资料：

[https://zhuanlan.zhihu.com/p/96631135](https://zhuanlan.zhihu.com/p/96631135)

[https://marklodato.github.io/visual-git-guide/index-zh-cn.html#basic-usage](https://marklodato.github.io/visual-git-guide/index-zh-cn.html#basic-usage)

[https://git-scm.com/book/zh/v2](https://git-scm.com/book/zh/v2)

[https://www.bilibili.com/video/BV1og4y1u7XU/?vd_source=2fd7d34bd95e75cdd841dff21f112683](https://www.bilibili.com/video/BV1og4y1u7XU/?vd_source=2fd7d34bd95e75cdd841dff21f112683)

## 什么是Git？

Git是一个流行的版本管理工具，可以帮助我们方便快捷地保存不同时期编辑的文件版本。举一个例子，第一天，老师布置了一个任务给我们，要求我们用python编写一个输出“HelloWorld”的程序。下面是我们的作业：

```python
print("Hello World")
```

第二天，老师觉得我们是中国人，还是要输出中文比较好。于是我们就在第一天的基础上进行修改，把下面的代码文件提交给老师：

```python
print("你好，世界")
```

第三天，老师觉得，输出“你好，世界挺没有意思的，要不输出一句古诗词吧。于是我们就在第二天的基础上进行修改，把下面的代码文件提交给老师:

```python
print("落霞与孤鹜齐飞，秋水共长天一色")
```

第四天，老师又说，python是美国人做出来的东西，还是用英语比较好。于是，我们又不得不把代码改成第一天的样子。

写过代码的人都知道，我们的代码经常需要修改。通常的情况是，这些代码改着改着就变成和原来完全不相同了。这个时候我们想要把代码恢复成原来的样子就非常地麻烦。有人就开始思考，能不能写一个程序，自动把当前的文件保存起来形成一个版本呢？这就是Git要做的事情。