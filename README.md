> 本仓库源码开源，你可以直接拿本仓库源码去进行魔改。
> 若你不懂怎么操作，我可以收费帮忙制作纪念日网站，欢迎来聊。QQ: 974393900

# 两周年纪念日网页

这个小小的网页是两周年纪念日的时候做的，送给女朋友，也是第一次做这种东西。最终女朋友看到了也被感动到了，有女朋友的程序猿们可以借鉴一下啦。

[http://rychouuuu.coding.me/two_year/](http://rychouuuu.coding.me/two_year/)

技术栈：

- create-react-app //react脚手架
- React
- ES6

文章使用打印机输出的效果，还给背景音乐加了时间控制，可以在指定时间开始播放。

想要达到撩人的效果，最重要的还是文字啦。

> 背景告白气球特效扒自网络，非自己编写。如有侵权请联系：974393900@qq.com

## 使用教程

> 下面步骤涉及到`Git`和`npm`的使用，如果你还不会用，请百度自学。

### 将本仓库克隆到本地

```shell
git clone https://github.com/Rychou/two_years
```

### 同步依赖

``` shell
npm install
```

### 启动项目

```shell
npm start
```

### 进行个性化编辑

这一步就可以对自己想要的纪念日期、背景音乐、文字等进行个性化编辑。

#### 纪念日

打开项目根目录下的`src/Main.js文件`，找到如下代码。

```js
componentDidMount() {
    this.print();
    setInterval(() => {
        this.time(2016, 4, 23) // 1.填写你们的纪念日
    }, 1000
    )
    var audio = document.getElementById("audio");
    setTimeout(() => audio.play(), 8500) // 背景音乐在页面加载后，延迟播放的时长，单位：毫秒。
}
```

#### 背景音乐

项目默认的背景乐是周董的《告白气球》，你也可以换成对方最喜欢的音乐。建议从网上找到音乐文件下载到`src/audio/`目录下，并且推荐`mp3`格式的文件，兼容性好。

将文件下载好后，打开`src/Main.js`，在文件开头，找到如下代码。

```js
import React, { Component } from 'react'
import $ from 'jquery'
import url from './audio/gbqq.mp3' // 引入背景音乐文件。填写文件路径。建议文件名用英文。
```

#### 网页标题和信封标题

修改网页标题，打开`public/index.html`，找到以下代码：

```html
<title>两周年纪念！</title> <!-- 将这里的文字替换成你想要的标题即可-->
```

修改信封标题，打开`src/App.js`，找到如下代码：

```html
<div className="text">你收到一封信，点击查收！</div> <!-- 将这里的文字替换成你想要的标题即可 -->
```

#### 核心：文章内容

最重要的部分其实是你的文字部分，其他的都不重要，重要是文字要走心。

打开`src/Main.js`，找到如下代码，将你要写的话，写到对应位置。

```jsx
<div className="date">{date()}</div>
    <div id="autotype">
        <h1 style={{ fontWeight: 900 }}>哈喽！wuli趴布猪！</h1> <!-- 文章开头文字 -->
        <p >在煽情开始之前，先放首歌当背景音乐吧！Music!</p> <!-- 文章内容 -->
        <p>今天是我们两周年的纪念日，从2016年4月23日到现在，我们一起经历了许许多多的事情，
        有欢笑也有争吵，也曾因为一些事情闹过分手，但是我们都走过来了。</p>
        <!-- 此处省略800字 -->
    </div>
```

### 打包编译

执行命令

```shel
npm run build
```

执行完后，会在`build`目录生成打包后的网页，你可以直接把这个打包后的网页当场给你女朋友看。但这就不能远程访问了。

若要远程访问，有两个办法：

1. 部署到远程服务器，不推荐，因为如果要用自己域名的话，需要备案。
2. 部署到Github Pages 或 Coding Pages，推荐，因为域名可不备案，没那么复杂，成本也更低。

### 部署到Github Pages

网上有很多文章讲这个东西，我这里不做过多详细的介绍，简单讲一下流程。

1. 在Github上创建一个空的仓库，以 userName.github.io 作为仓库名。其中 userName 是你的用户名。

2. 将仓库克隆到本地
3. 将刚刚打包编译后的网页（`build`目录下所有文件），复制粘贴到仓库根目录。
4. 用git push 到远程仓库。
5. 在仓库的设置页面，启动Github Pages服务。大概1分钟左右打开 https://userName.github.io 即可。

### 更骚的操作

你可以买自己的域名，比如常见的英文域名等。最骚的是，你可以买一个中文域名  **XXX.我爱你**。注意这是可行的。

只不过中文域名的配置稍微复杂一些，具体怎么操作我也不太记得了，但也不难，大家自行百度即可。

## 写到最后

这个网页是我在大二时期写的，现在已经准备大四了，也找到了自己心仪的前端岗位实习。

异地狗是正的很难受，当时我跟她相隔1300公里，在纪念日当天却不能相见，真是很难受。当时也不知道要送啥才好，于是想到自己也是程序员，那就用程序员的方式表达浪漫吧～

于是就写了这个网页，当时的代码现在看起来写的是很烂，也没有花太多心思去考虑代码，功能实现了就行了。如果大佬们见到了这么烂的代码别吐槽哈，我自己已经吐槽了自己了哈哈哈。

最后想祝愿各位不管是兄弟还是姐妹们，能够和另外一半长长久久，幸福美满！

> 如果大家在实现的时候遇到了什么问题，也欢迎邮件: 974393900@qq.com 或直接加 QQ也行。

## 捐赠：

<img src="https://user-images.githubusercontent.com/25195267/63184954-47da8080-c08b-11e9-8a25-07d2dfc929e3.png" width="150"/><br>
<img src="./public/img/alipay.jpg" width="150"/>

