---
layout: post
title: CIM(计算机集成制造)
category: 智能制造
keywords: 
---

## 什么是CIM 
Computer Integrated Manu-facturing：计算机集成制造，指在所有与生产有关企业部门中集成地用电子数据处理，CIM包括了在生产计划和控制、计算机辅助设计、计算机辅助工艺规划、计算机辅助制造、计算机辅助质量管理之间信息技术上的协同工作，其中为生产产品所必需的各种技术功能和管理功能应实理由集成。

CIM (Common Information Model通用信息模型），描述管理数据的语言和方法。CIM 架构包括系统、应用程序、局域网 (LAN) 和设备的模型。CIM 架构使不同开发人员在不同平台上开发的应用程序都能以标准格式描述管理数据，以便在多个管理应用程序中共享



1. CIM是一种组织，管理与运行企业生产的哲理，其宗旨是使企业的产品质量高、上市快、成本低、服务好、从而使企业赢得竞争。
2. 企业生产的各个环节，即市场分析、经营决策、管理、产品设计、工艺规划、加工制造、销售、售后服务等全部活动过程是一个不可分割的有机整体，要从系统的观点进行协调，进而实现全局优化。
3. 企业生产的要素包括人、技术及经营管理。其中，尤其要重视发挥人在现代化企业生产中的主导作用。
4. 企业生产活动中包括信息流（采集、传递和加工处理）及物流两大部分，现代企业中尤其要重视信息流的管理运行及信息流与物流间的集成。
5. CIM技术是基于现代管理技术、制造技术、信息技术、自动化技术、系统工程技术的一门综合性技术。具体讲，它综合并发展了企业生产各环节有关的计算机辅助技术，包括计算机辅助经营管理与决策技术、计算机辅助建模、仿真、实现技术及计算机辅助质量管理与控制技术等。


## 通用信息模型
(CIM,Common Information Model）是一个与具体实现无关的、用于描述管理信息的概念性模型。CIM分为两部分：CIM 规范（CIM Specification）和CIM 模式（CIM Schema）。CIM 规范提供了模型的正式定义，它描述了语言、命名、元模式和到其他管理模型（如SNMP MIB）的映射技术；CIM 模式则给出了实际模型的描述。CIM 模型由核心模型、公共模型和扩展模型三层构成。核心模型是一系列类、连接和属性的集合，该对象组提供了所有管理域通用的基本信息模型；公共模型提供特定管理域的通用信息模型，这些特定的管理域，如系统、应用程序、网络和设备等；扩展模型代表通用模型的特定技术扩展。

通过CIM 建模，能够得到管理域中实体的抽象和表示，包括它们的属性、操作和关系。这样的模型独立于任何具体的数据库、应用、协议以及平台。因此，CIM 模型要求不同开发商所提供的基于不同平台的应用都采用一种标准的格式来描述管理数据，以使数据能够在多种应用间共享。CIM 采用面向对象的方式构建了一种新的适用于管理系统、网络的结构和概念模型。CIM 建模是一种通用方法。特定管理域的CIM 建模是在核心模型和公共模型的基础上进行扩展。