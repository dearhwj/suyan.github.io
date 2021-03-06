---
layout: post
title: 工艺路线
category: 智能制造
---

## 正文
工艺路线用来表示企业产品在企业的一个加工路线（加工顺序）和在各个工序中的标准工时的定额情况。是一种计划管理文件，不是企业的工艺文件，不能单纯的使用工艺部门的工艺卡来代替。工艺卡主要是用来指定工人在加工过程中的各种操作要求和工艺要求，而工艺路线则强调加工的顺序和工时定额情况，主要用来进行工序排产和车间成本统计。



工艺路线，英文是Routing，是描述物料加工、零部件装配的操作顺序的技术文件，是多个工序的序列。工序是生产作业人员或机器设备为了完成指定的任务而做的一个动作或一连串动作，是加工物料、装配产品的最基本的加工作业方式，是与工作中心、外协供应商等位置信息直接关联的数据，是组成工艺路线的基本单位。例如，一条流水线就是一条工艺路线，这条流水线上包含了许多的工序。


在ERP系统中，工艺路线文件一般用以下内容进行描述：物品代码、工序号、工序说明、工作中心代码、排队时间、准备时间、加工时间、等待时间、传送时间、最小传送量、外协标识（Y/N）、标准外协费和工序检验标志（Y/N）等等字段。物料代码用来表示该工艺路线是针对何种物料的工艺路线。工序号用来表示该物料加工时需要经过多少个工序，该工序号应该按照加工顺序进行编排。工作中心代码，用来表示该工序在哪个工作中心中进行加工。排队时间、准备时间、加工时间、等待时间、传送时间五种作业时间，主要是用来描述工序的作业时间，以进行能力计算和车间作业排产。外协标识、标准外协费是指如果该工序（如电镀）对企业来说是进行外协加工的，需要在工艺路线中进行指定。
