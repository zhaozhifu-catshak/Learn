# HTTP 协议定义

a <label style="color:orange">stateless</label> application-level <label style="color:orange">requst/response </label>protocol that uses extensible semantics and <label style="color:orange">self-descriptive </label>message payloads for flexible interaction with network-based <label style="color:orange">hypertext infromation</label> system.
一种<label style="color:orange">无状态的</label>、应用层的、<label style="color:orange">以请求 / 应答</label>方式运行的协议，它使用可扩展的语义和<label style="color:orange">自描述</label>消息格式，与基于网络的<label style="color:orange">超文本信息</label>系统灵活地互动。

参考链接：https://tools.ietf.org/html/rfc7230


# 补充说明：

如果在 macOS 系统下运行 telnet 命令，会与 Xshell 下略有不同。

先输入：
```
  telnet www.taohui.pub 80
```
按回车键后会出现：
```
  Trying 116.62.160.193...
  Connected to www.taohui.pub.
  Escape character is '^]'.
```
然后再输入：
```
  GET /wp-content/plugins/Pure-Highlightjs_1.0/assets/pure-highlight.css?ver=0.1.0 HTTP/1.1
```
回车后继续输入：
```
  Host:www.taohui.pub
```
输入完毕后，按两次回车即可。
# ABNF(Augmented BNF) 官方文档
https://www.ietf.org/rfc/rfc5234.txt

巴科斯范式的英文缩写为 BNF，它是以美国人巴科斯 (Backus) 和丹麦人诺尔 (Naur) 的名字命名的一种形式化的语法表示方法，用来描述语法的一种形式体系，是一种典型的元语言。又称巴科斯 - 诺尔形式 (Backus-Naur form)。它不仅能严格地表示语法规则，而且所描述的语法是与上下文无关的。它具有语法简单，表示明确，便于语法分析和编译的特点。

# 课程相关资料下载地址
https://github.com/geektime-geekbang/geektime-webprotocol

# Windows 系统 Xshell  软件下载链接
https://www.netsarang.com/zh/xshell/

# macOS 系统安装 telnet 的方法
打开终端，先通过以下命令安装 [homebrew](https://brew.sh/index_zh-cn) 
```
  /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
安装完 homebrew 之后，运行  brew install telnet

# Wireshark 下载地址
https://www.wireshark.org/download.html




