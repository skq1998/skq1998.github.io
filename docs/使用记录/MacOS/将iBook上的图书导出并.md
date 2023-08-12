---
share: true
category: 使用记录/MacOS
---

## 问题

- 目前 iPad 和 iPhone 上的 iBook 并没有提供导出 epub 的选项
- Mac 上面可以直接将书拖出，但是这是 epub 被解压成了一个文件夹

> 这篇文章的目标在于将 iBook 解压的文件夹重新打包为一个 epub 文件夹

## 解决方案

从 iBook 中拖出图书到桌面，拖出来的其实是一个文件夹，后缀名为 `.epub`

![image_1_20230812164056.gif](../../assets/img/image_1_20230812164056.gif)

在终端中进入该文件夹

```shell
cd ~/Desktop/filename.epub
```

执行下面的命令

```shell
zip -0Xq  filename.epub mimetype
zip -Xr9Dq filename.epub *
```

现在，你可以在拖出来的文件夹中找到打包好的 epub 文件了