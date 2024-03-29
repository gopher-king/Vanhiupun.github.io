---
layout: post
title: Chrome、Edge 默认下载器也能多线程下载
categories: 浏览器
banner:
  image: https://vanhiupun.github.io/assets/images/banners/Chrome.png
  opacity: 0.618
  background: "#000"
  height: "50vh"
  min_height: "50vh"
  heading_style: "font-size: 2.25em; font-weight: bold; "
  subheading_style: "color: gold"
tags: [浏览器]
---
## 前言
大家在使用 Chrome、Edge 浏览器的时候，下载一些小文件往往都会直接用默认下载器，但是下载大文件的时候，一般都会搭配其他 专业多线程下载工具 使用，但是嫌麻烦...

最近我发现 Chrome、Edge 浏览器有个多线程下载选项，默认是关闭的，我试了下发现挺好用。

> **注意：任何基于 Chromium 内核的浏览器（国内套壳、Edge等）都支持该功能！**    

## 一键开启
- **Chrome 浏览器**: 地址栏输入并回车：`chrome://flags/#enable-parallel-downloading`
- **Edge 新版浏览器**: 地址栏输入并回车：`edge://flags/#enable-parallel-downloading`

就会看到如下图所示，将默认的 `Default` 改为 `Enabled` 即可！

**然后重启 Chrome 浏览器再去下载个文件试试速度吧！**

### 为什么下载速度没有翻倍？

- **该文件不允许多线程下载！**
> 例如，网站服务器限制了同一时间一个 IP 只能建立 1 个下载连接。

- **该文件没有显示文件总大小！**
> 部分网站下载文件时，不会显示文件总大小，这样的话就没办法多线程下载了（其他任何多线程下载工具都不行），没有文件总大小，就没办法等份分割文件进行并行下载。

### 多线程下载是什么？

一些人的可能并不清楚 多线程下载 是什么，我简单解释下。

目前的 专业下载工具(HTTP下载) 之所以下载速度更快，就是因为使用了 **多线程下载** 技术。
> 目前的 BT 软件也都支持 HTTP 多线程下载（因为 BT 下载上传也是需要文件分片）。

这个多线程下载技术很容易理解，那就是**将下载的文件分割成多份**。

假设下载一个 1GB 的文件，会被**分割为 8 个 128MB**的文件块（8线程为例），然后与服务器建立 8 个连接，同时下载这 8 个分割后的文件块，如果**单线程**时最多 1MB/s 下载速度，那么现在理论上你的下载速度就从**1MB/s 提高到了 8MB/s**。

这 8 个文件块都下载完成后，就会开始合并文件，这也是为什么**下载完成后总会停顿一会儿才会提示下载完成**。
