# bat [![translate-svg]][translate-list]

[translate-svg]: http://llever.com/translate.svg
[translate-list]: https://github.com/chinanf-boy/chinese-translate-list

「 一个`cat(1)`克隆与语法高亮和Git集成。 」

[中文](./readme.md) | [english](https://github.com/sharkdp/bat)


---


## 校对 ✅

<!-- doc-templite START generated -->
<!-- repo = 'sharkdp/bat' -->
<!-- commit = '84734eac9d19f90f942e587e7ec7d3aad4cda2c2' -->
<!-- time = '2018 8.30' -->
翻译的原文 | 与日期 | 最新更新 | 更多
---|---|---|---
[commit] | ⏰ 2018 8.30 | ![last] | [中文翻译][translate-list]

[last]: https://img.shields.io/github/last-commit/sharkdp/bat.svg
[commit]: https://github.com/sharkdp/bat/tree/84734eac9d19f90f942e587e7ec7d3aad4cda2c2

<!-- doc-templite END generated -->

### 贡献

欢迎 👏 勘误/校对/更新贡献 😊 [具体贡献请看](https://github.com/chinanf-boy/chinese-translate-list#贡献)

## 生活

[help me live , live need money 💰](https://github.com/chinanf-boy/live-need-money)

---

<p align="center">
  <img src="doc/logo-header.svg" alt="bat - a cat clone with wings"><br>
  <a href="https://travis-ci.org/sharkdp/bat"><img src="https://travis-ci.org/sharkdp/bat.svg?branch=master" alt="Build Status"></a>
  <img src="https://img.shields.io/crates/l/bat.svg" alt="license">
  <a href="https://crates.io/crates/bat"><img src="https://img.shields.io/crates/v/bat.svg?colorB=319e8c" alt="Version info"></a><br>
  一个 <i>cat(1)</i> 克隆与语法高亮和Git集成。.
</p>

### 目录

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


  - [语法突出显示](#%E8%AF%AD%E6%B3%95%E7%AA%81%E5%87%BA%E6%98%BE%E7%A4%BA)
  - [Git集成](#git%E9%9B%86%E6%88%90)
  - [自动分页](#%E8%87%AA%E5%8A%A8%E5%88%86%E9%A1%B5)
  - [文件连接](#%E6%96%87%E4%BB%B6%E8%BF%9E%E6%8E%A5)
- [如何使用](#%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8)
- [安装](#%E5%AE%89%E8%A3%85)
  - [在Ubuntu上](#%E5%9C%A8ubuntu%E4%B8%8A)
  - [在Arch Linux上](#%E5%9C%A8arch-linux%E4%B8%8A)
  - [在Void Linux上](#%E5%9C%A8void-linux%E4%B8%8A)
  - [在FreeBSD上](#%E5%9C%A8freebsd%E4%B8%8A)
  - [在macOS上](#%E5%9C%A8macos%E4%B8%8A)
  - [二进制文件](#%E4%BA%8C%E8%BF%9B%E5%88%B6%E6%96%87%E4%BB%B6)
  - [源项目](#%E6%BA%90%E9%A1%B9%E7%9B%AE)
- [定制](#%E5%AE%9A%E5%88%B6)
  - [突出主题](#%E7%AA%81%E5%87%BA%E4%B8%BB%E9%A2%98)
  - [输出风格](#%E8%BE%93%E5%87%BA%E9%A3%8E%E6%A0%BC)
  - [添加新语法/语言定义](#%E6%B7%BB%E5%8A%A0%E6%96%B0%E8%AF%AD%E6%B3%95%E8%AF%AD%E8%A8%80%E5%AE%9A%E4%B9%89)
  - [添加新主题](#%E6%B7%BB%E5%8A%A0%E6%96%B0%E4%B8%BB%E9%A2%98)
  - [使用不同的页面方式](#%E4%BD%BF%E7%94%A8%E4%B8%8D%E5%90%8C%E7%9A%84%E9%A1%B5%E9%9D%A2%E6%96%B9%E5%BC%8F)
- [故障排除](#%E6%95%85%E9%9A%9C%E6%8E%92%E9%99%A4)
  - [终端和颜色](#%E7%BB%88%E7%AB%AF%E5%92%8C%E9%A2%9C%E8%89%B2)
- [开发](#%E5%BC%80%E5%8F%91)
- [项目目标和替代方案](#%E9%A1%B9%E7%9B%AE%E7%9B%AE%E6%A0%87%E5%92%8C%E6%9B%BF%E4%BB%A3%E6%96%B9%E6%A1%88)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

### 语法突出显示

`bat`支持大量编程和mark**语言的语法突出显示: 

![Syntax highlighting example](https://imgur.com/rGsdnDe.png)

### Git集成

`bat`与`git`沟通,显示关于修改的索引 (参见左侧栏) : 

![Git integration example](https://i.imgur.com/2lSW4RE.png)

### 自动分页

如果输出对于一个屏幕来说太大,`bat`可以控制自己的输出`less`管道,. 

### 文件连接

哦..你也可以用它来连接文件: wink:. 每当`bat`检测到非交互式终端,它将回退到打印普通文件内容. 

## 如何使用

在终端上显示单个文件

```bash
> bat README.md
```

一次显示多个文件

```bash
> bat src/*.rs
```

从stdin读取,明确指定语言

```bash
> yaml2json .travis.yml | json_pp | bat -l json
```

```bash
> curl -s https://raw.githubusercontent.com/sharkdp/bat/master/src/main.rs | bat -l rs
```

作为`cat`的替代品: 

```bash
bat > note.md  # quickly create a new file

bat header.md content.md footer.md > document.md

bat -n main.rs  # show line numbers (only)

bat f - g  # output 'f', then stdin, then 'g'.
```

## 安装

### 在Ubuntu上

*一些和其他基于Debian的Linux发行版.*

从[发布页面](https://github.com/sharkdp/bat/releases),下载最新的`.deb`包裹,并通过以下方式安装: 

```bash
sudo dpkg -i bat_0.6.0_amd64.deb  # adapt version number and architecture
```

### 在Arch Linux上

你可以安装[该`bat`包](https://www.archlinux.org/packages/community/x86_64/bat/),官方来源: 

```bash
pacman -S bat
```

### 在Void Linux上

你可以安装`bat`通过xbps-install: 

    xbps-install -S bat

### 在FreeBSD上

您可以安装预编译的[`bat`包](https://www.freshports.org/textproc/bat)用pkg: 

```bash
pkg install bat
```

或者在FreeBSD上,自己构建它: 

```bash
cd /usr/ports/textproc/bat
make install
```

### 在macOS上

你可以安装`bat`,通过[brew](http://braumeister.org/formula/bat): 

```bash
brew install bat
```

### 二进制文件

看[发布页面](https://github.com/sharkdp/bat/releases),其中预建版本的`bat`,有许多不同的架构. 

### 源项目

如果你想建立`bat`的源代码,您需要Rust 1.26或更高版本. 然后你可以使用`cargo`建立一切: 

```bash
cargo install bat
```

在macOS上,您可能必须安装`cmake` (`brew install cmake`) 以便构建一些依赖项. 

## 定制

### 突出主题

使用`bat --list-themes`获取语​​法突出显示的所有可用主题的列表. 选择`TwoDark`主题,运行`bat`带`--theme=TwoDark`选项或设置`BAT_THEME`环境变量为`TwoDark`. 在你的shell启动文件中使用`export BAT_THEME="TwoDark"`,使更改永久化. 

### 输出风格

你可以使用`--style`这个外观的选项,控制`bat`输出. 您可以使用`--style=numbers,changes`例如,仅显示 Git更改和行号 ,但没有网格和文件头. 

### 添加新语法/语言定义

`bat`使用优秀的语法高亮的库[`syntect`](https://github.com/trishume/syntect/). `syntect`可以阅读任何[Sublime Text的`.sublime-syntax`文件](https://www.sublimetext.com/docs/3/syntax.html)和主题. 要添加新语法定义,请执行以下操作. 

使用语法定义文件创建一个文件夹: 

```bash
BAT_CONFIG_DIR="$(bat cache --config-dir)"

mkdir -p "$BAT_CONFIG_DIR/syntaxes"
cd "$BAT_CONFIG_DIR/syntaxes"

# Put new '.sublime-syntax' 语言定义文件
# in this folder (or 它的 子目录), for example:
git clone https://github.com/tellnobody1/sublime-purescript-syntax
```

现在使用以下命令将这些文件解析为二进制缓存: 

```bash
bat cache --init
```

最后,使用`bat --list-languages`检查新语言是否可用. 

如果您想要返回默认设置,请使用: 

```bash
bat cache --clear
```

### 添加新主题

这与我们添加新语法定义的方式非常相似. 

首先,使用新语法突出显示主题创建一个文件夹: 

```bash
BAT_CONFIG_DIR="$(bat cache --config-dir)"

mkdir -p "$BAT_CONFIG_DIR/themes"
cd "$BAT_CONFIG_DIR/themes"

# 下载一个主题是 '.tmTheme' 格式, for example:
git clone https://github.com/greggb/sublime-snazzy

# Update the binary cache
bat cache --init
```

最后,使用`bat --list-themes`检查新主题是否可用. 

### 使用不同的页面方式

`bat`使用在`PAGER`环境变量中,指定的页面方式. 如果未设置此变量,`less`就是默认使用. 如果要使用其他页面方式,可以修改`PAGER`变量或设置`BAT_PAGER`环境变量,以覆盖在中指定的内容`PAGER`. 如果要将命令行参数传递给页面方式,则需要创建一个 小的shell脚本 作为包装器,例如: 

```bash
#!/bin/bash

less --tabs 4 -RF "$@"
```

## 故障排除

### 终端和颜色

`bat`控制终端*有*和*无*真彩色支持. 但是,语法高亮主题中的颜色未针对8位颜色进行优化,因此强烈建议您使用具有24位真彩色支持的终端 (`terminator`,`konsole`,`iTerm2`,...) . 看到[本文](https://gist.github.com/XVilka/8346728)了解更多详情和完整的支持truecolor的终端列表. 

确保你的truecolor终端,设置了`COLORTERM`变量到`truecolor`或者`24bit`. 除此以外,`bat`将无法确定是否支持24位转义序列 (并回退到8位颜色) . 

## 开发

```bash
# Recursive clone to retrieve all submodules
git clone --recursive https://github.com/sharkdp/bat

# Build (debug version)
cd bat
cargo build

# Run unit tests and integration tests
cargo test

# Install (release version)
cargo install

# 构建 bat 二进制文件, 若修改了的语法和主题
bash assets/create.sh
cargo install -f
```

## 项目目标和替代方案

`bat`试图实现以下目标: 

-   提供美观,高级的语法高亮
-   与Git集成以显示文件修改
-   是 (POSIX)`cat` 的直接替代品
-   提供用户友好的命令行界面

如果你正在寻找类似的程序,有很多选择. 看[这个文件](doc/alternatives.zh.md)进行比较. 
