

## 前言

Kubernetes是一个流行的容器编排工具。它将多个分散的计算机组合成一个大型的计算资源，并且构造了一种通过Kubernetes 应用程序接口（API）来对资源进行访问的方式。Kubernetes是一个源自Google，过去五年，在云原生计算基金会(CNCF) (https://www.cncf.io/)主持下，由大量的合作者合作开发的开源软件。

Operator通过扩展Kubernetes来自动化管理特定应用程序的整个生命周期。Operators作为打包装置向Kubernetes上的分布式应用程序提供服务，并负责监控，维护，恢复和升级部署的软件。



## 本书目标读者

如果你在Kubernetes集群上部署应用程序，你会非常熟悉形成Operator这种模式的一些困难和灵感。如果你维护过类似数据库和文件系统这样的基础服务，他们不在你的编排集群内，但是你又想把他们带到你的集群里，那么这本Kubernetes Operator指南就是为你准备的。



## 本书涵盖范围

这本书解释了Operator是什么以及Operators是如何扩展Kubernetes API的。书中会演示如何部署和使用现有的Operators，以及如何使用红帽(Red Hat) Operator框架(*https://github.com/operator-framework*)为你的应用程序创建和分发Operators.我们讲述关于设计，构建，以及分发Operators的好的做法，并且解释通过网站可靠性管理(SRE)的原则使得Operators更有生命力的想法。

在第一章节介绍Operators以及相关的概念之后，我们提出了几个访问Kubernetes集群的方法，在集群上你可以进行本书其余部分的练习。通过Kubernetes集群，你可以部署一个Operator，观察他在应用程序失败，扩容或者升级到一个新版本时的行为表现。

稍后，我们会探索一下Operator SDK，向你展示如何使用SDK来构建一个Operator来把一个示例应用程序赋予为一个Kubernetes的一等公民(first-class citizen)。有了以上的实践基础之后，我们会讨论引出Operators的SRE理念，以及他们共有的目标：减少操作的工作量和成本，增加服务的稳定性，通过把团队从重复性的维护工作中解放出来以刺激团队的创新工作。



## Operator框架和SDK

Operator的模式是在CoreOS (*https://coreos.com*) ，为了自动化处理Kubernetes集群上不断增长的复杂应用程序而出现的，包括管理Kubernetes本身，以及核心的etcd (*https://github.com/coreos/etcd*) 键值存储。CoreOS被Red Hat收购之后，Operators的工作也一直在进行，最终在2018年发布了开源的Operator框架和SDK。书中的示例使用了Red Hat的Operator SDK，并且在Operator 框架中加入了Red Hat Operator SDK的分发机制。





## 其他的Operator工具

社区围绕着Operator的发展已经相对成熟了，拥有100多个Operators为大量的应用程序使用，这些Operators来自多个供应商，以及Red  Hat的分发渠道。也有一些其他的Operator 构建工具，这里就不详细讨论了，但是读完本书之后，你可以把它们跟Operator SDK和Operator 框架做一下比较。其他的构建Operators的开源工具有Python的 Kopf (*https://oreil.ly/JCL-S*)，来自Kubernetes项目的Kubebuilder(*https://oreil.ly/8zdbj*) ，以及 Java Operator SDK (*https://oreil.ly/yXhVg*)。





## 排版约定

本书使用了下列排版约定

- 斜体(Italic)

  表示新术语，网站链接，电子邮件地址，文件名称和文件扩展名。

- 等宽字体(Constant width)

  用于程序片段，段落中出现的程序元素，像变量，函数名，数据库，数据类型，环境变量，声明，以及关键字。

- 加粗等宽字体

  表示由用户输入的命令或者其他文本。

-  等宽斜体

  显示应该被用户提供的值或者由上下文决定的值替换的文本



   图标表示提示或者建议

   图标表示普通的笔记

   图标表示注意事项



## 使用示例代码







## 鸣谢

我们要感谢Red Hat和 OpenShift Advocacy 小组的支持，尤其是Ryan Jarvinen的坚定、全面的帮助。我们也感谢参与审查，核对，建议的许许多多的朋友们，是他们付出他们的时间让这本书更加连贯完整，感谢其中的Anish Asthana, Evan Cor‐ dell, Michael Gasch, Michael Hausenblas, Shawn Hurley, 和 Jess Males。



















