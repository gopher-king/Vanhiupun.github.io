---
layout: post
title: 在命令行运行 VSCode（macOS）
categories: VS Code
banner:
  image: https://vanhiupun.github.io/assets/images/banners/vscode.png
  opacity: 0.618
  background: "#000"
  height: "50vh"
  min_height: "50vh"
  heading_style: "font-size: 4.25em; font-weight: bold; "
  subheading_style: "color: gold"
tags: [VS Code,命令行,终端]    
---
#### 安装code命令后，可在终端使用"code --path"用vscode打开当前目标文件夹。</br>
### 安装方式
`vscode` 中执行 `shift+command+p`，打开命令面板，键入 `shell` ，选择 `“在PATH中安装code命令”` ，如下图</br>
![在PATH中安装code命令](https://vanhiupun.github.io/assets/images/banners/code-shell.png) </br>

### 使用方式

安装完成后，在终端输入类似如下命令
```c++
md ~/Desktop/code
touch ~/Desktop/code/test.html
code ~/Desktop/code
```

或者是cd到当前目录使用 `code .` 即可打开
```bash
cd ~/Desktop/code
code .
```

在命令行里使用 `code --help` 查看帮助
![在命令行里使用 `code --help` 查看帮助](https://vanhiupun.github.io/assets/images/banners/code-cmd.png) </br>
