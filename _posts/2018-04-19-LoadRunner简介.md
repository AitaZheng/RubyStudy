---
layout: detail
title: LoadRunner简介
descritption: 总体架构及工作原理
tags: core
category: core
---

## LoadRunner简介
### LoadRunner是一种预测系统行为和性能的负载测试工具。通过以模拟上千万用户实施并发负载及实时性能监测的方式来确认和查找问题，LoadRunner能够对整个企业架构进行测试。企业使用LoadRunner能最大限度地缩短测试时间，优化性能和加速应用系统的发布周期。 LoadRunner可适用于各种体系架构的自动负载测试，能预测系统行为并评估系统性能。

## LoadRunner总体架构
### LoadRunner的总体架构图,从图中可以看出组件VUGen, Controller和Analysis之间的关系
![loadrunner总体架构图](/Users/Aita/Documents/loadrunner总体架构图.jpg "loadrunner总体架构图")


### LoadRunner主要组成部分
- Vuser Generator(虚拟用户发生器)：

Vuser Generator是一个集成开发环境,用于录制回放修改Vuser脚本

- Controller(压力调度和监控中心)：

Controller是一个框架程序和监控程序,负责将Vuser脚本以多进程/多线程方式在Load Generator机器上运行

- Load Generator(压力产生器）：

模拟多用户并发访问被测试系统的组件。

- Analysis(压力结果分析工具)：

Analysis是一个数据分析工具，对测试过程中收集到的各种性能数据进行计算、汇总和处理，生成各种图表和报告，为系统性能测试结果分析提供支持。

## LoadRunner工作原理
### Loadrunner工作原理，从图中可以看出如何利用LoadRunner进行一次典型的系统性能测试
![LoadRunnner工作原理图](/Users/Aita/Documents/loadrunner工作原理图.jpg "loadrunner工作原理图")

### LoadRunner测试流程
1. 用户确定进行测试的业务或者交易,录制并生成脚本
2. 手工修改脚本,确定脚本能回放成功
3. 在Controller中对场景进行配置,启动测试,Controller控制Load Generator对被测系统的加压方式和行为
4. Controller负责搜集被测系统各个环节的性能数据.各个Load Generator会记录最终用户相应时间和脚本执行的日志
5. 压力测试运行结束以后, Load Generator将数据传送到Controller中,由Controller对测试数据进行汇总
6. 用Analysis对数据进行分析
7. 对系统进行调优,重复进行压力测试,确定性能是否有所提高

###  LoadRunner的内部流程图，从图中可以看出LoadRunner内部各个组件之间如何进行交互,数据流和文件流之间如何进行.
![loadrunner内部流程图](/Users/Aita/Documents/loadrunner内部流程图.jpg "loadrunner内部流程图")

 
