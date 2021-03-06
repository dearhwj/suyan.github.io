---
layout: post
title: 里特定律 - Little's Law
category: 数学和算法
keywords: 里特定律 
---

## 正文
里特定律（Little's Law）源自排队理论，是IT系统性能建模中最广为人知的定律。

里特定律揭示了前置时间（Lead Time）、在制品数量（Work In Progress, WIP）和吞吐率（Throughput）之间的关系。

Little s Law

前置时间 - Lead time：只请求进入到系统 与 请求验收完成之间的时间段。前置时间按照所经过的时间（分钟、小时等）来度量。一个请求可以是一个需求、一个用户故事、一个异常、物料、一个来自用户的请求等。
在制品数量 - Work in progress (WIP)：正在被处理的请求（工作单元）数量，正在被处理指这些请求已经进入到系统中，但是还没有产出。
吞吐率 - Throughput：在一确定时间内离开系统的工作单元数量，例如3个用户故事/天。
此定律的总结相当有意思并重要：

WIP越大，前置时间越长，即要完成已经开始的工作需要更长的时间。换言之，为了满足开发或服务的截止时间，我们必须减少在制品数量，或者在开始新工作之前完成在制品。

然而，在很多情况中发生了恰好相反的情况：为使整个项目可以“跑”得更快，团队开始处理更多任务。希望保持大量进行中工作的另一个原因是：以此来达到高资源利用率。

无论什么原因，假设吞吐率不发生变化，在制品的增加会使完成在制品所需的时间（即前置时间）同时增加。

尽管看起来违反直觉，但需要记住的是：降低WIP有助于满足SLA并降低开发前置时间。

专注于降低前置时间有助于识别已经开展的无用活动。消除这些无用活动会产生两种积极影响：
（1）消除流程中的浪费
（2）降低总WIP，从而进一步缩短前置时间并带来更高效的开发。 

吞吐率越高，前置时间越短

有很多不同的途径来提升性能：自働化增值活动（自働化非增值活动等同于自働化浪费的产生），改进流程并增加更多资源。如果你决定增加更多资源，需要观察整体前置时间，因为增加额外资源会同时增加在制品数量。

每种精益（Lean）倡议都会试图最小化浪费并缩短生产周期。缩短生产周期等价于缩短前置时间。最小化浪费包括对当前库存的分析以及减少库存的相关步骤，这等价于降低WIP。
为什么这个定律对项目经理很重要？

里特定律是了解软件开发团队或软件运营团队真实性能的工具。
提供可预测性
例如，如果我们必须实现50个需求，团队的平均能力是5个需求/周，我们所需的时间是：
50 个需求 / 5 个需求每周 = 10 周。
揭示了工作批量越大，处理时间（前置时间）越长。
解释了为什么多任务导致延期而非加速工作完成。
通常人们相信，并行开展多个任务能够提升生产力。因此，许多公司中共同的做法是将多个任务分配给一个人。然而，与机器不同的是，人类并不善于以并行处理的方式执行。增加在制品还会增加某项任务修改和返工的时间，从而降低吞吐率。最终，工作执行所需的时间不够了，并且已经开始但还未结束的工作开始堆积。
简言之，里特定律有利于找到在制品与前置时间之间的平衡。
为达到最佳WIP限制提供了基础。 如果WIP限制低于最佳水平，就会有未充分利用的资源并且性能低下。如果WIP限制超出了最佳水平，工作单元就开始在队列中堆积并同样是性能降低。
有助于理解阻塞一项工作或必须解决错误对项目或服务截至时间的影响。这两种情况都会降低吞吐率并因此增加前置时间。
应用里特定律的重要条件：
里特定律非常有用，但是除了解公式之外，你必须了解到使用里特定律必须满足的条件：

所有参数都使用平均值：平均前置时间、平均WIP和平均吞吐率
单位必须一致：即，如果我们按一周来度量吞吐率，前置时间也必须按周及，WIP同理。
系统必须稳定：即，所有进入系统的工作必定会离开系统；总WIP在这段时间内守恒，工作平均到达率等于工作平均离开率。
总之，正确的使用里特定律可以有助于获得平稳的工作流，并提升项目和IT服务的可预测性。在制品数量（WIP）是影响项目性能和软件开发或服务完成所需时间的关键因素。限制WIP降低前置时间，此外还会减少工作流程中的浪费。

### 参考资料
[https://www.cnblogs.com/lchrennew/p/Littles-Law.html](https://www.cnblogs.com/lchrennew/p/Littles-Law.html)