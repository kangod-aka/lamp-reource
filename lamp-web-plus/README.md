# lamp 快速开发平台

[![AUR](https://img.shields.io/badge/license-Apache%20License%202.0-blue.svg)](https://github.com/zuihou/lamp-cloud/blob/master/LICENSE) [![](https://img.shields.io/badge/作者-zuihou-orange.svg)](https://github.com/zuihou) [![](https://img.shields.io/badge/版本-3.1.1-brightgreen.svg)](https://github.com/zuihou/lamp-cloud) [![GitHub stars](https://img.shields.io/github/stars/zuihou/lamp-cloud.svg?style=social&label=Stars)](https://github.com/zuihou/lamp-cloud/stargazers) [![star](https://gitee.com/zuihou111/lamp-cloud/badge/star.svg?theme=white)](https://gitee.com/zuihou111/lamp-cloud/stargazers) [![GitHub forks](https://img.shields.io/github/forks/zuihou/lamp-cloud.svg?style=social&label=Fork)](https://github.com/zuihou/lamp-cloud/network/members) [![fork](https://gitee.com/zuihou111/lamp-cloud/badge/fork.svg?theme=white)](https://gitee.com/zuihou111/lamp-cloud/members)

# lamp 项目名字由来

## 叙事版：

在一个夜黑风高的晚上，小孩吵着要出去玩，于是和`程序员老婆`一起带小孩出去放风，路上顺便讨论起项目要换个什么名字，在各自想出的名字都被对方一一否决后，大家陷入了沉思。走着走着，在一盏路灯下，孩砸盯着路灯打破宁静，喊出：灯灯～ 我和媳妇愣了一下，然后对视着一起说：哈哈，这个名字好～

## 解释版：

`灯灯`： 是我小孩学说话时会说的第一个词，也是我在想了很多项目名后，小孩一语点破的一个名字，灯灯象征着光明，给困境的我们带来希望，给加班夜归的程序员们指引前方～

`灯灯`(简称灯， 英文名：lamp)，他是一个项目的统称，包含以下几个子项目

## lamp 项目组成

### 工具集

注意： 请先下载 lamp-util 代码并编译（mvn install） 到本地仓库，然后在编译（mvn install）lamp-cloud 或 lamp-boot 项目， 最后编译（mvn install）lamp-job 项目！！！

### 工具集 （lamp-util 项目必备，其他 2 个可选）

| 项目 | gitee | github | 备注 |
| --- | --- | --- | --- |
| 工具集 | [lamp-util](https://gitee.com/zuihou111/lamp-util) | [lamp-util](https://github.com/zuihou/lamp-util) | 业务无关的工具集，cloud 和 boot 项目都依赖它 |
| 代码生成器 | [lamp-generator](https://gitee.com/zuihou111/lamp-generator) | [lamp-generator](https://github.com/zuihou/lamp-generator) | 给开发人员使用 |
| 定时调度器 | [lamp-job](https://gitee.com/zuihou111/lamp-job) | [lamp-job](https://github.com/zuihou/lamp-job) | 尚未开发 |

### 后端 （下面 2 个项目功能一致，任选其一即可）

| 项目 | gitee | github | 备注 |
| --- | --- | --- | --- |
| 微服务版(后端) | [lamp-cloud](https://gitee.com/zuihou111/lamp-cloud) | [lamp-cloud](https://github.com/zuihou/lamp-cloud) | SpringCloud 版 |
| 单体版(后端) | [lamp-boot](https://gitee.com/zuihou111/lamp-boot) | [lamp-boot](https://github.com/zuihou/lamp-boot) | SpringBoot 版(和 lamp-cloud 功能基本一致) |

### 前端 （下面 3 个项目功能一致，任选其一即可）

| 项目 | gitee | github | 备注 | 演示地址 |
| --- | --- | --- | --- | --- |
| 中后台管理系统 | [lamp-web](https://gitee.com/zuihou111/lamp-web) | [lamp-web](https://github.com/zuihou/lamp-web) | （全部功能已完成）基于 vue-admin-element | http://tangyh.top:10000 |
| 中后台管理系统 | [lamp-web-beautiful](https://gitee.com/zuihou111/lamp-web-beautiful) | [lamp-web-beautiful](https://github.com/zuihou/lamp-web-beautiful) | （正在开发...）基于 vue-admin-beautiful | http://tangyh.top:180 |
| 中后台管理系统 (强烈推荐！👏👏👏) | [lamp-web-beautiful](https://gitee.com/zuihou111/lamp-web-plus) | [lamp-web-beautiful](https://github.com/zuihou/lamp-web-plus) | （正在开发...）基于 vue-vben-admin （vue 3 + vite 2） | http://tangyh.top:3100 |

# lamp-web 简介

`lamp-web` 的前身是`zuihou-ui` + `zuihou-admin-ui`，从 3.0.0 版本开始，将 2 个系统合并为`lamp-web`，它是`lamp`项目的其中一员。原来在 zuihou-admin-ui 系统的功能已经合并到内置租户【0000】，账号【lamp_pt】中。

`lamp-web` 是 [lamp-cloud](https://github.com/zuihou/lamp-cloud) 和 [lamp-boot](https://github.com/zuihou/lamp-boot) 2 个后台项目共用的管理后台，仅需在启动时调整`vue.config.js`文件中的代理。它基于[vue element admin](https://panjiachen.github.io/vue-element-admin-site/zh/)构建。

## lamp 会员版项目演示地址

- 地址： http://tangyh.top:3100
- 以下内置账号仅限于内置的 0000 租户
- 平台管理员： lamp_pt/lamp (内置给公司内部运营人员使用)
- 超级管理员： lamp/lamp
- 普通管理员： general/lamp
- 普通账号： normal/lamp

> ps: 演示环境中内置租户没有写入权限，若要在演示环境测试增删改，请使用 lamp_pt 账号查询租户管理员账号后,登录新租户测试

## lamp-cloud/lamp-boot + lamp-web-plus 功能介绍：

1. 租户管理：运营人员管理所有的租户创建
2. 工作台：普通用户常用功能
3. 组织管理：组织、岗位、用户数据维护、重置用户密码等
4. 资源中心：消息、短信、附件管理
5. 流程管理：流程部署、模型管理、流程示例
6. 系统设置：菜单、资源配置、角色管理、给角色绑定用户、给角色授权菜单和资源、字典、地区、系统参数、操作日志、登录日志、应用管理等
7. 网关设置：限流和阻止访问
8. 开发者管理：定时任务、接口文档、注册&配置中心、服务监控、数据库监控、zipkin 监控、SkyWalking 监控

## 技术栈

- Vue 3.x
- vuex 4.x
- typescript 4.x
- ant-design-vue 2.x
- axios 0.21.x
- echarts 5.x
- vite 2.x

## 安装

### 环境要求

- `Node.js`: - 版本大于 `12.0.0`
- `yarn` : - 包管理工具.

### 下载

```
//  使git对文件名大小写敏感
git config core.ignorecase false

// 拉取项目代码

git clone https://github.com/zuihou/lamp-web-plus.git

cd lamp-web-plus

// 如果使用别的包管理工具，可以自行安装
// 如果未安装yarn，请运行：npm install -g yarn
yarn install
```

## 使用

### 开发环境

```bash
yarn serve
```

### 打包

```bash

yarn build # 打包

yarn build:no-cache # 打包，执行之前会先删除缓存

yarn report # 生成构建包报表预览
```

### 格式化

```bash
yarn lint:stylelint # 样式格式化

yarn lint:prettier # js/ts代码格式化
```

### 其他

```bash
yarn reinstall # 删除依赖重新装，兼容window

yarn preview # 本地进行打包预览

yarn log # 生成CHANGELOG

yarn clean:cache # 删除缓存

yarn clean:lib # 删除node_modules，兼容window系统
```

# 交流群，加群前请先给项目点个 "Star"，谢谢！😘

- 63202894(主群 满员请加群 2)
- 1011148503(群 2)

# 如果觉得本项目对您有任何一点帮助，请点右上角 "Star" 支持一下， 并向您的基友、同事们宣传一下吧，谢谢！

# 详细文档: https://www.kancloud.cn/zuihou/zuihou-admin-cloud

    ps: gitee捐献 或者 二维码打赏(本页最下方)： 45元及以上 并 备注邮箱，可得开发文档一份(支持后续更新)
        打赏或者捐献后直接加群：1039545140 并备注打赏时填写的邮箱，可以持续的获取最新的文档。

# 遇到问题请先查看历史 issue，未找到解决方案，在提交 issue(问题描述详细一些，报错截图大一些，复现步骤全一些)

    https://github.com/zuihou/lamp-cloud/issues

# 友情链接 & 特别鸣谢

- 微服务快速开发平台：[https://github.com/zuihou/lamp-cloud](https://github.com/zuihou/lamp-cloud)
- 单体快速开发平台：[https://github.com/zuihou/lamp-boot](https://github.com/zuihou/lamp-boot)
- MyBatis-Plus：[https://mybatis.plus/](https://mybatis.plus/)
- knife4j：[http://doc.xiaominfo.com/](http://doc.xiaominfo.com/)
- hutool：[https://hutool.cn/](https://hutool.cn/)
- xxl-job：[http://www.xuxueli.com/xxl-job/](http://www.xuxueli.com/xxl-job/)
- kkfileview：[https://kkfileview.keking.cn](https://kkfileview.keking.cn)
- vue-vben-admin： [https://github.com/anncwb/vue-vben-admin](https://github.com/anncwb/vue-vben-admin) lamp-web-plus 基于本项目改造
- FEBS Cloud Web： [https://gitee.com/mrbirdd/FEBS-Cloud-Web](https://gitee.com/mrbirdd/FEBS-Cloud-Web) lamp-web 基于本项目改造， 感谢 [wuyouzhuguli](https://github.com/wuyouzhuguli)
- Cloud-Platform： [https://gitee.com/geek_qi/cloud-platform](https://gitee.com/geek_qi/cloud-platform) 作者学习时接触到的第一个微服务项目
