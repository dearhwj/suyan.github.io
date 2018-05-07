---
layout: post
title: 混沌工程
category: 软件架构和设计
keywords: 混沌工程
---


## 原文
原文地址：[https://segmentfault.com/a/1190000013682325#articleHeader2](https://segmentfault.com/a/1190000013682325#articleHeader2)

混沌工程（Chaos Engineering）是指在生产环境的分布式系统中进行一些试验，用以考验系统在动荡环境下的健壮性，从而增强对系统稳定运行的信心。

### 导语
随着大型分布式软件系统的进步，软件工程的最佳实践也随之改变。
在分布式行业中，我们能够迅速地响应增加开发灵活性和部署快速化的做法。但这些做法带来效益的同时，也带来了另一个紧迫问题：我们到底有多少把握来确保投产的复杂系统能够正常工作呢？

即便是分布式系统中每个独立的服务都正常工作，服务之间的相互调用也仍然可能造成不可预期的结果。这些结果在现实中可能很少发生，但是一旦发生就会影响整个生产环境，使得整个分布式系统变得混乱不堪。

因此，我们有必要在造成系统级别的异常结果之前，就先发现系统的这些弱点。它们通常会以下面这些形式出现：

服务不可用时，因回退设置不当而导致错误
由于不恰当的超时设置酿成重试风暴
因下游依赖收到过大流量造成的服务中断
由于单点故障奔溃导致的级联系统坍塌
我们必须主动定位那些影响最大的弱点，而且要在它们对用户造成不利影响之前就找出来。我们需要一种方式来管理这些系统的固有混沌，在保证不断增加灵活性和响应速度的同时，做到最后不管系统有多复杂，我们仍然能够对生产部署充满信心。

拥有一个经验导向、同时立足于系统的方法，不仅可以有效定位分布式系统中的混沌问题，还可以对这些系统承受现实考验的能力建立起信心。
我们从受控的试验中习得分布式系统运行行为的过程，称为混沌工程。

混沌实践
为了有针对地定位大规模分布式系统中的不确定性，混沌工程可以看做是用于帮助发现系统性弱点的试验。这些试验包含以下四个步骤：

定义描述系统正常工作的稳态（Steady State），它们必须是可测量的系统输出
假设对照组和实验组在实验过程中都将会保持稳态
引入跟现实类似的影响因素，如服务器崩溃、硬盘故障和网络断开等
通过对比对照组和实验组之间稳态的差异来反驳步骤 2 中的假设
稳态破坏起来越困难，我们对系统就越有信心。如果实验过程发现了系统弱点，那我们就有了改进目标，以避免它在整个系统中引发错误。

实践原则
下面这些原则描述了混沌工程的理想应用。聪明的你可能已经发现，上文说的混沌实验其实已经应用了这些原则。越是严格地遵循这些原则，那我们对分布式系统稳健运行地信心就越强。

一、 基于稳态行为建立假设

应聚焦于系统的可测量输出，而不是系统的内部属性。系统的稳态由对输出的短期测量结果构成。整个系统的吞吐量、错误率、延时百分比等都可以成为代表系统稳态的行为表现。试验过程中，通过关注这些系统表现模式，混沌因素验证了系统确实在正常工作，而不是在验证系统是如何工作。

二、 模拟多样的真实事件

混沌变量应该反应真实世界的事件。应该通过潜在影响或估计频率来确定事件的优先顺序。考虑的事件可以是跟硬件故障的，比如服务器死机；可以是跟软件错误相关的，比如错误的响应；也可以是非故障事件，比如流量高峰或低峰。任何能够破坏稳态的事件都是混沌试验的一个潜在变量。

三、 在生成环境试验

系统的行为会因环境不同和流量大小而表现不一。由于这些行为随时可能发生变化，因此对真实流量进行采样是唯一能够反映真实情况的办法。为了同时保证系统运行方式的真实性和当前部署系统的相关性，混沌工程强烈推荐直接在生产流量上进行试验。

四、 可持续的自动化试验

手动运行混沌试验是劳动密集型操作，而且也是不可持续的。应该让混沌试验自动化，并且能够可持续运行。混沌工程应该在试验和分析中都集成进自动化操作，让一切可自动化的都实现自动化。

五、 最小化影响范围

在生产上进行试验可能会导致不良的用户体验影响。尽管一些短期的负面影响在所难免，但混沌工程师有责任也有义务要把影响降到最低，而且要做到运筹帷幄。

混沌工程是个非常强大的工程实践，它已经在世界上一些大规模项目中改变着软件的设计和实现。在分布式系统领域，其他的工程实践正追逐着快速化和灵活性，然而混沌工程却特别地处理着系统不确定性。混沌原则不仅增强了大规模快速创新地信心，同时也为保证了客户应有的良好体验。