###首次提交fork自：[https://gitcafe.com/ops](https://gitcafe.com/ops)
###原作者：[UlricQin](http://ulricqin.com)
<br/>
fork已经过原作者同意。

---
##简介
该项目主要用来管理各服务器上的各个业务系统的agent，并非部署agent。（一个部署agent应该有更加复杂的逻辑和功能）

因此建议在装机初始化的时候，就进行updater的安装。

meta可支持横向扩展。

##Feature
- 轻量，简单有效
- 支持版本
- 支持横向扩展
- 支持小流量环境测试
- 支持自定义

##架构
本项目分为**updater**和**meta**两部分：

- updater部署于机器上，作为一个agent，负责管理各业务的agent，同时与meta进行交互。
- meta作为服务端，接收来自updater的心跳请求，同时根据请求的机器来返回应该部署的相应版本。
