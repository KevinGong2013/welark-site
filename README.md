# 彩虹桥🌈

本指南为集成[微信客服](https://kf.weixin.qq.com)到[飞书](https://open.feishu.cn), 如果你在查找其他文档请查看

[微信客服](https://kf.weixin.qq.com) -> [飞书](https://open.feishu.cn)
[微信客服](https://kf.weixin.qq.com) -> [钉钉](https://www.dingtalk.com)
[微信客服](https://kf.weixin.qq.com) -> [企业微信](https://open.feishu.cn)
[微信客服](https://kf.weixin.qq.com) -> 个人微信

## 飞书创建企业自建应用

彩虹桥使用飞书自建应用的机器人链接微信客服，因此开始之前你需要[创建应用]()

创建应用成功以后你需要进行以下操作

### 应用凭证

点击左边的凭证与基础性西

- App ID
> copy备用

- App Secret
> copy备用
### 权限管理

- 通讯录权限范围 
> 选择需要管理微信客服的员工

- 权限配置
> 机器人需要在消息群组发送/接受消息
在飞书权限配置栏点击 【消息与群组】然后勾选所有权限，点击批量开通(共17项)

### 事件订阅

- Encrypt Key
> 点击重置按钮生成新的key，然后copy备用

- Verification Token
> 点击查看，然后copy备用


### 发布
点击左边的版本管理与发布创建新版本提交审核， 然后选择申请线上发布

## 部署应用

为了数据安全彩虹桥不提供任何云服务，需要企业自己购买云服务部署。你也可以购买彩虹桥官方提供的部署服务。

彩虹桥目前只支持通过docker部署

```shell
docker pull ghcr.io/kevingong2013/welark:v0.9.2
```

在这里查看最新版本 https://github.com/KevinGong2013/welark/pkgs/container/welark