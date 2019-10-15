# 测试网重新搭建

目前测试网使用的版本最低要求是主网force-v1.7.1版本．建议使用github上面的最新代码编译出来的最新版.

测试网根结点P2P地址：147.52.71.18：11000

**此地址将在测试网完全启动以后关闭**

# 编译启动
与主网启动类似，需要注意的是测试网启动所需的genesis文件与主网不同.

启动命令：./nodeos --config-dir=./config --data-dir=./data

# 原来有测试网节点启动流程

## 1.更换config

将config文件夹中的genesis.json替换为原来的genesis.json。
config.ini文件可以使用文件夹中的config.ini文件，也可以把p2p-peer-address地址修改为p2p-peer-address = 47.52.71.18:11000

## 2.选择一份空的data文件夹启动节点

使用命令./nodeos --config-dir=./config --data-dir=./data 启动节点

## 3.BP帐户创建

可以把公钥发给开发团队来创建帐户，开发团队会给新的帐户打测试币以便测试网的功能的调用。创建完帐户以后注册BP并给BP投票，然后修改config.ini
添加：
```config.ini从
producer-name = BPBANE
signature-provider = 公钥=KEY:私钥
```
重启节点为出块节点。

**producer-name和signature-provider可以配置2个，也就是一个node可以作为2个BP的程序端**
