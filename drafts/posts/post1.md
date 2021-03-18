---
title: Python开发环境搭建：Atom
categories:
- python
tags:
- python
url: https://zhuanlan.zhihu.com/p/354278905
---

![](https://i.loli.net/2021/03/04/9LQRKVMfGP2gzTX.jpg)

## 安装文本编辑器Atom

入坑Sublime、VSCode无数次后，还是回头选择了Atom IDE，因为它颜值惊艳、操作便捷、界面简单，除了一般编辑器都有的代码折叠和自动补全，还自带原生Markdown支持！！！这漂亮的实时预览和代码高亮真让人春心荡漾！并且，插件非常丰富！

于是，果断选择Atom作为鸽婆的**创作神器**，为Python开发之旅保驾护航！
<!--more-->
官网一键安装：[AtomSetup-x64](https://atom.io/)

确认操作系统无误，点击download，打开下载好的AtomSetup-x64.exe，极速体验！

![缺点是启动速度不如sublime](https://pic2.zhimg.com/v2-e2e305deea69303a19d71da452138945_b.png)


## 失足卡顿的惨痛经历

此时你一定急不可耐地冲向Install a Package，风风火火地下载了一堆插件：minimap用来预览全貌，atom-beautify用来格式化（想到令人头痛的html），file-icons小图标好可爱呀，material主题貌似很热门吼，markdown-preview-enhanced吊打我的Typora呢（Typora是我常用的md编辑器），script可以运行代码嗷，autocomplete-python自动补全呢，python-autopep8调格式也不错哟，linter-flake8检查语法错误呢，Hydrogen简直是jupyter的孪生姐妹……你在界面乐此不疲地倒腾……

[Atom热门主题排行榜](https://atom.io/themes/list?direction=desc&sort=downloads)：material、monokai、seti。

[Atom热门插件排行榜](https://atom.io/packages/list?direction=desc&sort=stars)：

![atom官网除了主页美丽，其他页面都设计得不忍直视](https://pic3.zhimg.com/v2-67ae3f6b8e594fd04c342a862fceed4a_b.png)

A few hours later...

突然，你意识到此时的atom一片混乱卡顿缓慢，再也不是当初清纯活泼的模样！你蹙起眉，两行清泪润湿了乌黑的下眼眶！

一怒之下，你卸载了atom，并剿杀了一切软件残留：[如何彻底删除atom](https://cn.compbs.com/how-uninstall-atom-windows)，[如何更彻底地删除](https://www.coder.work/article/552966)！

## 正确的打开方式是什么？

那么，配置环境和安装插件的正确方式是什么呢？

1. 打开Editor Settings，**勾选Scroll Past End和Show Indent Guide，设置Tab Length为4，Font Size为20**，护眼第一啦！
2. 主题我喜欢atom自带的**One Light，**打开themes->One Light UI->Settings->**Font Size设置为15**，语法主题我选择**Monokai**。还是为了护眼！码字时还可以随时ctrl+和ctrl-调整字体大小。
3. 下载插件：**minimap、file-icons、atom-beautify、markdown-preview-enhanced、python-autopep8**。大道至简，这是我目前选择的基础组件，可能以后会更新！进入python-autopep8->Settings，勾选Format On Save。

![atom-material-syntax-dark语法主题也好看，只是Python语法高亮略丑，就不放了](https://pic3.zhimg.com/v2-62a1e257adc2ca9978dee539798d3342_b.png)



个人认为，**编辑器只需提供高效、舒适的代码体验即可**，script等运行代码的功能比较鸡肋，反而会加重的负担。

**下面重点来了，下载插件的方式！！！**

打开cmd，执行以下命令（apm是Atom Package Manager的缩写）：

```
pip install autopep8
apm install monokai, minimap, file-icons, atom-beautify, markdown-preview-enhanced, python-autopep8
```

如果一起下载速度太慢，也可以`apm install <package_name>`分开下载。

晃悠了一杯茶的时间，已经全部done啦！Voila！

重启Atom，Ctrl+Shift+P打开Settings->Packages，是不是整齐陈列着我们要的插件呢？（不知为什么ctrl+逗号不能打开settings）

码上行动叭！！！

![这是最终的windows界面](https://pic3.zhimg.com/v2-873f85f52366e6ab44b3eda548930102_b.png)



另外，有童鞋选择github上面的源码git clone，然后cd进文件夹、npm install来安装，也不错呢~

对了，卸载插件的话，`apm uninstall <package_name>`就好啦！


## 使用Github远程版本控制

最后解锁atom连接github和git！多么良心的日志啊！

话说，atom本来就是github开发的编辑器好嘛！我们来测试下好用吗！

Github注册无须多言吧，我创建了一个新的repository，命名blog，用来云端存储我的写作素材与稿件。这时我们看到页面提供了一系列指令：

![这里其实是blog仓库，但我为了演示又重新建了名为test的仓库](https://pic1.zhimg.com/v2-6daf82cf178c578fd4cf4c19da68cb88_b.png)


我们只需要打开windows系统的git bash，一句一句输入。我输入的是以下指令：

```
cd blog
echo "#blog" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/MissFreak/blog.git
git push -u origin main
```

成功后，在Atom打开blog这个文件夹（也就是你想要进行版本控制的项目），我们看到右侧显示github登录界面，提示我们打开github.atom.io，复制GitHub token到Atom的登录表单。Success！

![](https://pic1.zhimg.com/v2-6e1aa37602728c2eb6bdc8701b013270_b.png)

接下来就随心所欲地增改文件，然后stage all->commit to main->pull 吧！

终于不用在终端敲指令，也可以和Github Desktop说拜拜啦！

![](https://pic4.zhimg.com/v2-713ea328565e6babf7e9559c20bc2e8b_b.png)

**参考资料：**

[Atom Documentation-GitHub package](https://flight-manual.atom.io/using-atom/sections/github-package/)

----

**键盘之下，妙笔生花**

[正则表达式进阶！第一弹！](http://mp.weixin.qq.com/s?__biz=MzIzMDY0NDQ1Ng==&mid=2247485867&idx=1&sn=6d59acaeb3a6e9d4c324989c04c6ae62&chksm=e8b1062cdfc68f3a83b1f708414928b027fe5bcca4440d8c512fe197f306d1fdc42d0a68a9bf&token=1061934211&lang=zh_CN#rd)

[大扫盲！Python正则表达式实操！](http://mp.weixin.qq.com/s?__biz=MzIzMDY0NDQ1Ng==&mid=2247485654&idx=1&sn=7475f7247ecc6ecb2eadca474c82cfb3&chksm=e8b10751dfc68e47b23c45c51728c1518546603fcca73be7555be2d91edf193ff3b5772d68bc#rd)

[干货 | 正则表达式入门](http://mp.weixin.qq.com/s?__biz=MzIzMDY0NDQ1Ng==&mid=2247484919&idx=1&sn=7309a9bf1be78ea3250838724ebaa81c&chksm=e8b10a70dfc683666f6d87e6fda6f51863dbaf565ac522b6d01d80059c01a821af70bc279438&scene=21#wechat_redirect)
