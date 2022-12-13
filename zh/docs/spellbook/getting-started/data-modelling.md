---
title: 数据建模
---

这是构建魔法中最重要的一步。

一个魔法可以让您和其他用户更便捷地完成数据分析，它可以是一张表，更理想的话可以是一个数据视图。

构建魔法有诸多好处：

* **一致性和可维护性。** 对于临时的数据分析来说，复制其他现有的查询并重新编合是很有效的做法，但并非是一个长久之计。想象一下，如果您在您的查询中发现了一个错误，或者在智能合约上发现了一些新变化。 您可以更新_您自己的_查询，但每个分叉或复制该查询的用户都不会获得更新。

* **提高了指标的清晰度。** 每个指标通常都有好几种方式可以计算。 如果每个人都用自己的方案去计算一个指标，那么这个指标就很难被统一的定义和接受，同时这么做也消耗了大家许多时间去完成重复的工作。而魔法是在公共 GitHub 存储库上以完全透明的方式构建，这意味着社区可以就指标定义及实现达成一致。

* **简洁性以及更好的开发体验** 谁会想一遍又一遍地编写重复的查询？把无趣的重复工作进行自动化可以让开发者更专注于数据分析中的关键部分。[DRY 开发方式](https://www.softwareyoga.com/is-your-code-dry-or-wet)也可以像适用于其他编程语言一样适用于 SQL 编写。

这些迹象表明是时候该施展（构建）魔法了:

* 当您有多个查询包含相同的子查询时。
* 您在多个查询中复用非常长的静态值列表。
* 该查询已被分叉和复制了许多次。
* 您的查询中包含十分复杂的运算逻辑，在其他地方能被有效复用。