---
title: "Hexo Next主题配置汇总"
tags:
- hexo
- markdown
---

2021年3月10日博客配置完毕。在此记录网上有关hexo主题和markdown的教程。后来我重新配置了一次，只修改了三个文件：_config.yml和next/_config.yml以及表格设置（当然还有css/images不过这个是公开可见的）。

然后是**修改文章内链接文本样式**、**文章内单行代码的样式设置**等等，我们只需要新建一个styles.styl文件即可，需要在custom_file_path中加入这个地址。

<!-- more -->
<br />

<center><img src="https://i.loli.net/2021/03/17/Z5CrHdz438AmbxG.png"  alt="" width="700" /></center>

在里面写下：

```css
code {
    padding: 2px 4px;
    border-radius: 4px;
    margin-right: 2px;
    margin-left: 2px;
    background-color: rgba(27, 31, 35, 0.05);
    font-family: "Operator Mono", Consolas, Monaco, Menlo, monospace;
    word-break: break-all;
    color: #ef5777;
}

.post-body h2 {
  display: inline-block;
  font-weight: bold;
  background: black;
  color: #ffffff;
  padding: 5px 10px 5px;
  margin-right: 3px;
  font-size: 1.2em;
}


// 文章内链接文本样式
.post-body p a{
  color: #ef5777;
  border-bottom: none;
  border-bottom: 1px solid #ef5777;
  &:hover {
    color: #fc6423;
    border-bottom: none;
    border-bottom: 1px solid #fc6423;
  }
}

.post-body strong {
    display: inline;
    padding: 0.2em 0.6em 0.3em;
    font-size: 80%;
    font-weight: bold;
    line-height: 1;
    color: #fff;
    text-align: center;
    white-space: nowrap;
    vertical-align: baseline;
    border-radius: 5px;
    background-color: #ef5777;
}

.post-body u {
    font-weight: bold;
    text-decoration: none;
}

```







更改表格：

https://www.granneman.com/webdev/coding/css/centertables

```css
/*tables.style*/

```

```
D:\project\hexo>npm list
hexo-site@0.0.0 D:\project\hexo
+-- hexo-browsersync@0.3.0
+-- hexo-deployer-git@3.0.0
+-- hexo-filter-emoji@2.2.2
+-- hexo-generator-archive@1.0.0
+-- hexo-generator-category@1.0.0
+-- hexo-generator-index-pin-top@0.2.2
+-- hexo-generator-searchdb@1.3.3
+-- hexo-generator-tag@1.0.0
+-- hexo-helper-live2d@3.1.1
+-- hexo-math@4.0.0
+-- hexo-reference@1.0.4
+-- hexo-renderer-ejs@1.0.0
+-- hexo-renderer-kramed@0.1.4
+-- hexo-renderer-mathjax@0.6.0
+-- hexo-renderer-pandoc@0.3.0
+-- hexo-renderer-stylus@2.0.1
+-- hexo-server@2.0.0
+-- hexo-symbols-count-time@0.7.1
+-- hexo-theme-landscape@0.0.3
+-- hexo-wordcount@6.0.1
+-- hexo@5.4.0
`-- live2d-widget-model-wanko@1.0.5
```



更改字体：

https://spartazhc.github.io/2020/06/03/Next%E4%B8%BB%E9%A2%98%E5%AD%97%E4%BD%93%E9%85%8D%E7%BD%AE/

文章置顶：
https://juejin.cn/post/6844904037465194503

图片操作：
https://davidwells.io/snippets/how-to-align-images-in-markdown
https://www.w3schools.com/html/html_images.asp

其他美化：
https://huangpiao.tech/2019/01/24/Hexo%E5%8D%9A%E5%AE%A2%E4%BC%98%E5%8C%96%E4%B9%8BNext%E4%B8%BB%E9%A2%98%E7%BE%8E%E5%8C%96/

Markdown进阶：

https://blog.csdn.net/thither_shore/article/details/52181464

https://unnamed42.github.io/2015-12-02-Markdown%E7%9A%84%E6%AD%A3%E7%A1%AE%E4%BD%BF%E7%94%A8%E6%96%B9%E5%BC%8F.html

https://blog.csdn.net/m0_37925202/article/details/80461714

Markdown使用html
https://www.wuchenxu.com/2015/12/30/Markdown-html-compare/

支持数学公式：

https://www.jianshu.com/p/9b9c241146bc