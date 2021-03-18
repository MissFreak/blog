---
layout: "post"
title: "【进阶】用Flask开发的API并部署到Heroku"
date: "2021-03-10 17:24"
tags:
- api
- flask
- python
- heroku
---

# 部署Flask开发的API到Heroku
上篇文章我们介绍了如何用flask开发简单的web api，下面我们把它部署到heroku上，方便更多人使用。

参考官方教程：https://devcenter.heroku.com/articles/getting-started-with-python

以及这个技术博客：http://www.bjhee.com/flask-heroku.html

windows上部署参考（建议使用git bash）：https://caijialinxx.github.io/2018/07/25/deploy-on-heroku/

**步骤总结：**

- 注册[Heroku帐号](https://signup.heroku.com/)
- 下载客户端
- 在本地命令行登录
  - 如果出现IP Address Mismatch，复制并粘贴`heroku login -i`到终端用邮箱密码登录
- 创建应用
- 部署应用
  - `cd D:\Users\virtualenv\flask-api`;  `git init `
  - `echo "web: gunicorn run:app --log-file -" > Procfile`
- 访问应用地址

# 进阶版应用











参考文献：



