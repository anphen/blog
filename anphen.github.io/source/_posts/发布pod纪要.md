---
title: 发布pod纪要
---
# **发布个人pod纪要**
* 1.登录Pod账号：`pod register email`
* 2.注册pod账号：`pod register email name`
* 3.clone库到本地，添加原始文件，打上标签，push远端库
* 3.创建spec：`pod spec create specname`
* 4.验证spec正确性：`pod spec lint  specname  --verbose --use-libraries --allow-warnings`

-------

##### 更新只需要进行以下步骤
5.打上tag，用新版本tag值修改spec中s.version，push远端库
6.发布pod:`pod trunk push specname --use-libraries --allow-warnings --verbose`
7.添加拥有者: `pod trunk add-owner pod库名 用户email`


