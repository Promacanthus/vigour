# VIGOUR

使用领域驱动设计开发微服务。

## shipping

项目原始链接，[shipping](https://github.com/go-kit/kit/tree/master/examples/shipping)。

此示例展示了一个更贴近真实世界的应用程序，它由多个服务组成。

### 描述

该实现基于Eric Evans的《[领域驱动设计](http://www.amazon.com/Domain-Driven-Design-Tackling-Complexity-Software/dp/0321125215)》一书中的集装箱运输领域，该书最初是用Java实现的，但此后已移植到Go。本示例是一个简化版本，以演示Go kit的用法。原始的[Go应用程序](https://github.com/marcusolsson/goddd)是单独维护的，并带有AngularJS应用程序和模拟路由服务。

### 项目组织

该应用程序包含三个应用程序服务，即预订，处理和追踪。如前面的示例所示，每一个都是单独的Go kit服务。

- booking服务：货运公司用来预订和运送货物。
- handing服务：员工在全球范围内进行收货，装货注册。
- tracking服务：客户用来追踪路线上的货物。

也有一些通用领域服务，其中包含一些复杂的业务逻辑。它们提供每个应用程序服务使用的领域对象和服务，以为用户提供有趣的用例。

`inmem`是通用领域服务中存储库的内存实现。

`routing`提供了一个领域服务，该领域服务用于向外部应用程序查询可能的路由。

## 关于项目

为什么要创建这个项目呢？

因为，在学习领域驱动设计和微服务架构的时候，各种大佬的参考项目都是用Java写的。确实Java的生态更加成熟，在应用层开发的时候，用起来更方便吧。但是，看看现在云基础设施哪一个不是用Golang开发的（各大云原生开源项目疯狂暗示），那应用层用Go开发是不是能更好的和基础设施融合呢？我也不知道是不是这样，但是总想给Gopher证明一下，因此有了这个项目。

一来把学的知识用项目实践一下，二来查漏补缺，也当作笔记，最后希望给想要入门的人一个参考。

本项目参考如下项目（站在巨人的肩膀上走的更远）：

1. [shippy](https://github.com/EwanValentine/shippy)
2. [chitchat](https://github.com/nonfu/chitchat)
3. [goddd](https://github.com/marcusolsson/goddd)

## 使用的知识和技术

### 技术

- [go-kit](https://promacanthus.netlify.app/%E5%BC%80%E5%8F%91%E6%A1%86%E6%9E%B6/go-kit/)
- [gin](https://gin-gonic.com/zh-cn/docs/)
- [grpc](https://promacanthus.netlify.app/%E5%BC%80%E5%8F%91%E6%A1%86%E6%9E%B6/grpc/)
- [protocol-buffer](https://promacanthus.netlify.app/%E5%BC%80%E5%8F%91%E6%A1%86%E6%9E%B6/protocol-buffers/)

### 快速阅读

没时间的点这里，了解大概。有时间的看下面，了解透彻。

- [领域驱动设计](https://promacanthus.netlify.app/%E5%BE%AE%E6%9C%8D%E5%8A%A1/%E9%A2%86%E5%9F%9F%E9%A9%B1%E5%8A%A8%E8%AE%BE%E8%AE%A1/)
- [微服务业务](https://promacanthus.netlify.app/%E5%BE%AE%E6%9C%8D%E5%8A%A1/%E5%BE%AE%E6%9C%8D%E5%8A%A1%E4%B8%9A%E5%8A%A1/)
- [微服务平台](https://promacanthus.netlify.app/%E5%BE%AE%E6%9C%8D%E5%8A%A1/%E5%BE%AE%E6%9C%8D%E5%8A%A1%E5%B9%B3%E5%8F%B0/)

### 领域驱动设计

- https://dddcommunity.org/
- https://martinfowler.com/tags/domain%20driven%20design.html
- [《领域驱动设计：软件核心复杂性应对之道》](https://book.douban.com/subject/26819666/)

### 微服务

- https://microservices.io/
- [《微服务架构设计模式》](https://book.douban.com/subject/33425123/)

