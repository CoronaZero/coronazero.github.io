---
title: Git 使用 GPG 签名提交时，找不到 KEY
date: 2025-02-16 11:58:06
tags: 
- GPG
- Windows
- Git
- 编程
categories: 编程技术
---

# 问题...

初次入坑 GPG ，发觉这个东西很好用，既可以用来签名自己的文件 or 文本，也可以对这些进行加密操作，十分方便。

于是就想要在 GitHub 上提交代码时，使用 GPG 进行代码的签名操作。

结果在使用 VS code 提交代码时，报错提示找不到 KEY ，但是我确认我的 KEY 存在且能正常使用。

经过一番搜索……最终发现是 Git 似乎没有使用我另外安装的 GPG for Windows ，所以提示找不到 KEY。

# 解决方案

其实很简单，指定所使用的 GPG 程序的绝对路径就可以了，命令如下：

```
git config --global gpg.program "c:/Program Files (x86)/GnuPG/bin/gpg.exe"
```

请注意将以上命令中的路径替换为自己电脑上的路径！

另外，可以使用

```
git config commit.gpgsign true
```

来使得此仓库默认使用 GPG 签名提交代码。