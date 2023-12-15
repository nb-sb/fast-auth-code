# FastAuthCode

## 验证码管理平台

### 简介

用户将系统快速接入验证码功能，例如接入滑动验证码，点击验证码等，过滤机器人以及一些脚本攻击



### 使用的工具

MySQL存贮信息：用户账号，用户key，剩余验证次数，用户拥有所属系统

```
uid
username
password
remain
ownership_system
```

```
id
//系统名称 name
//用于系统验证的后端ip ip
```

Redis 存贮验证码生成的验证信息,如是否验证等

操作mysql数据库都用异步处理，所以操作数据库的耗时几乎可以忽略，

redis中 

​	1. //用户剩余次数 key: key value: 剩余次数

​	2.//验证码id是否验证成功 key: codeId value: bool 

逻辑条件

1.生成验证码时不修改用户剩余数量，验证成功时进行减少redis中用于剩余数量，并且异步修改mysql中数据


### 快速使用：

​	1.前端引入js,css文件

```
引入链接.js
引入链接.css
```

​	2.后端引入工具类文件

```

```

​	3.前端触发验证按钮

​	4.自己业务后端加入一个请求这个工具类进行验证是否验证成功了验证码




#### 安装教程

1.  xxxx
2.  xxxx
3.  xxxx

#### 使用说明

1.  xxxx
2.  xxxx
3.  xxxx

#### 参与贡献

1.  Fork 本仓库
2.  新建 Feat_xxx 分支
3.  提交代码
4.  新建 Pull Request


#### 特技

1.  使用 Readme\_XXX.md 来支持不同的语言，例如 Readme\_en.md, Readme\_zh.md
2.  Gitee 官方博客 [blog.gitee.com](https://blog.gitee.com)
3.  你可以 [https://gitee.com/explore](https://gitee.com/explore) 这个地址来了解 Gitee 上的优秀开源项目
4.  [GVP](https://gitee.com/gvp) 全称是 Gitee 最有价值开源项目，是综合评定出的优秀开源项目
5.  Gitee 官方提供的使用手册 [https://gitee.com/help](https://gitee.com/help)
6.  Gitee 封面人物是一档用来展示 Gitee 会员风采的栏目 [https://gitee.com/gitee-stars/](https://gitee.com/gitee-stars/)
