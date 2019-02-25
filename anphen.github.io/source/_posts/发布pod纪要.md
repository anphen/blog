---
title: 发布pod纪要
date: 2017-6-1
tags: 综合
---
# **发布个人pod纪要**

* 1.首次使用 Trunk 时，需要注册自己的电脑：

```
# pod trunk register [E-mail] [User Name]
$ pod trunk register zxlx276@163.com "anphen"
```
执行命令以后，上述邮箱会收到一封验证邮件，按照邮件说明打开制定的链接，注册流程就完成了。

* 2.注册流程完成后，可以使用命令查看注册信息：`pod trunk me`

* 3.clone库到本地，添加原始文件，打上标签，push远端库
* 3.创建spec：`pod spec create specname`
* 4.验证spec正确性：`pod spec lint  specname  --verbose --use-libraries --allow-warnings`

-------

##### 更新只需要进行以下步骤
* 5.打上tag，用新版本tag值修改spec中s.version，push远端库
* 6.发布pod:`pod trunk push specname --use-libraries --allow-warnings --verbose`

##### 其他
* 7.添加拥有者: `pod trunk add-owner pod库名 用户email`
* 8.搜索发布的库：`pod search ZXPageView`
* 9.查看库信息（版本记录和拥有者）：`pod trunk info WZMarqueeView`

