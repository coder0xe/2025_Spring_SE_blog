# <div align="center">[T.18]团队项目：Beta阶段项目总结</div>

| 项目                                 | 内容                                                         |
| ------------------------------------ | ------------------------------------------------------------ |
| 这个作业属于哪个课程                 | [2025年春季软件工程（罗杰、任健）](https://edu.cnblogs.com/campus/buaa/BUAA_SE_2025_LR/) |
| 这个作业的要求在哪里                 | [[T.18] 团队项目：Beta阶段项目总结](https://edu.cnblogs.com/campus/buaa/BUAA_SE_2025_LR/homework/13464) |
| 我在这个课程的目标是                 | 学习软件工程知识和软件开发中的通用方法，提升实际项目开发的能力，参与从需求分析、设计、编码、测试到维护的完整软件开发流程，并完成一个完整、实用、好用的软件 |
| 这个作业在哪个具体方面帮助我实现目标 | Beta阶段项目总结                                             |

## 一、设想和目标

1. 我们的软件要解决什么问题？是否定义得很清楚？是否对典型用户和典型场景有清晰的描述？
   * 缺乏一站式文献阅读和笔记记录的平台
   * 是
   * 是
2. 我们达到目标了么（原计划的功能做到了几个？ 按照原计划交付时间交付了么？ 原计划达到的用户数量达到了么?)

   * Beta阶段功能全部完成
   * 按照计划时间交付
   * 已经用户测试，但用户规模不大
3. 和上一个阶段相比，团队软件工程的质量提高了么？ 在什么地方有提高，具体提高了多少，如何衡量的？

   * 提高了
   * 在团队代码规范、项目管理等方面，通过飞书文档、github issue等衡量
4. **用户量, 用户对重要功能的接受程度和我们事先的预想一致么? 我们离目标更近了么?**

   * 一致
   * 离目标更近了

​	**有什么经验教训? 如果历史重来一遍**, **我们会做什么改进**?

​	用户量比较小，我们会更早进行发布并进行更广泛渠道的宣传，不止局限于微信水群宣传。

## 二、计划

1. 是否有充足的时间来做计划?  

   * 是

2. 团队在计划阶段是如何解决同事们对于计划的不同意见的？

   * 开讨论会

3. 你原计划的工作是否最后都做完了? 如果有没做完的，为什么?

   * 是

4. 有没有发现你做了一些事后看来没必要或没多大价值的事?

   * 写了个基于github action的代码风格检测
   * 部分接口没有商量清楚

5. 是否每一项任务都有清楚定义和衡量的交付件?

   * 是

6. 是否项目的整个过程都按照计划进行，项目出了什么意外？有什么**风险**是当时没有估计到的，为什么没有估计到? 

   * 更新服务器上的数据库和API token之后构建docker失败
   * 没有估计到重新构建docker镜像失败，因为之前没有调研过相关业务

7. 在计划中有没有留下缓冲区，缓冲区有作用么?

   * 有，让项目更加充分的测试

8. 将来的计划会做什么修改？（例如：缓冲区的定义，加班）

   * 整合不同页面时花费很多时间，需要留出更多的缓冲区

​	**我们学到了什么? 如果历史重来一遍**,**我们会做什么改进**?

代码能跑就别动！重复一遍：代码能跑就别动！



## 三、资源

1. 我们有足够的资源来完成各项任务么?

   * 有，服务器资源足够
2. 各项任务所需的时间和其他资源是如何估计的，精度如何?

   * 根据经验估计，具体到小时
   * 精度比较好
3. 测试的时间，人力和软件/硬件资源是否足够? 对于那些不需要编程的资源 (美工设计/文案)是否低估难度? 

   * 足够
   * 由前端同学统一设计，完成的较为良好
4. 你有没有感到你做的事情可以让别人来做（更有效率）?

   * 有，部分前端模块存在分工问题，但出于整体性只能自己来做

​	**有什么经验教训? 如果历史重来一遍**,**我们会做什么改进**?

​	Beta阶段分工较为合理，可以做的一点改进是降低人员流动性，专人负责专事。

## 四、变更管理

1. 每个相关的员工都及时知道了变更的消息?

   * 在微信群中及时通知

2. 我们采用了什么办法决定“推迟”和“必须实现”的功能?

   * 依据杀手功能还是辅助功能

3. 项目的出口条件（Exit Criteria – 什么叫“做好了”）有清晰的定义么? 

   * 有，见Beta阶段功能说明书的验收标准

4. 对于可能的变更是否能制定应急计划?

   * 是

5. 员工是否能够有效地处理意料之外的工作请求？
   * 是

​	**我们学到了什么? 如果历史重来一遍**, **我们会做什么改进**?

​	在微信群中收到了要及时回复收到。

## 五、设计/实现

1. 设计工作在什么时候，由谁来完成的？是合适的时间，合适的人么？

   * 功能设计工作在选题阶段完成，大家开会研讨
   * 页面设计由前端完成
   * 是合适的时间、合适的人
2. 设计工作有没有碰到模棱两可的情况，团队是如何解决的？

   * 前端页面设计有遇到
   * 大家共同商量，从用户角度考虑
3. 团队是否运用单元测试（unit test），测试驱动的开发（TDD）、UML, 或者其他工具来帮助设计和实现？这些工具有效么？ 比较项目开始的 UML 文档和现在的状态有什么区别？这些区别如何产生的？是否要更新 UML 文档？

   * 运用了单元测试
   * 有效
   * 我们使用UML画了项目交互时序图，项目开始和现在变化不大，证明功能设计比较合理
4. 什么功能产生的Bug最多，为什么？在发布之后发现了什么重要的bug? 为什么我们在设计/开发的时候没有想到这些情况?

   * 文献管理功能，原因是文献管理页面的层级结构比较复杂，同时对于组件库还需要进行修改

* 因为没有进行实践，问题是在实践中出现的

5. 代码复审（Code Review）是如何进行的，是否严格执行了代码规范？
   * 由PM进行代码复审
   * 我们使用了ES-lint进行前端代码风格检测

**我们学到了什么? 如果历史重来一遍,我们会做什么改进?**

* 我们学到了用户场景驱动开发。需要在开发同时进行及时测试。

## 六、测试/发布

1. 团队是否有一个测试计划？为什么没有？

   * 有

2. 是否进行了正式的验收测试？

   * 有

3. 团队是否有测试工具来帮助测试？

   * 有，Apifox

  很多团队用大量低效率的手动测试，**请提出改进计划**：至少一个方面的测试要用自动化的测试工具，自动化的测试结果报告，比较测试结果的差异，等等。 

​	使用pytest等进行单元测试，后端使用python模拟大量用户向服务器发送请求。

4. 团队是如何测量并跟踪软件的效能（Performance）的？压力测试（Stress Test）呢？ 从软件实际运行的结果来看，这些测试工作有用么？应该有哪些改进？

   * 观察数据返回时间
   * 压力测试使用软件JMETER
   * 有用，应该找一些更好用的测试软件

5. 在发布的过程中发现了哪些意外问题？

   * https的nginx代理问题

​	**我们学到了什么? 如果重来一遍,我们会做什么改进?**

​	设置覆盖率更高的单元测试，对更多的性能场景上压力测试。

## 七、团队的角色，管理，合作

1. 团队的每个角色是如何确定的，是不是人尽其才？

   * 根据大家个人意愿优先分配，算是人尽其才

2. 团队成员之间有互相帮助么？ 

   * 有

3. 当出现项目管理、合作方面的问题时，团队成员如何解决问题？

   * 通过开讨论会，微信交流等方式

4. 每个成员明确公开地表示对成员帮助的感谢 ： 

* 高悠然：我感谢 _____韩昕睿______对我的帮助， 因为某个具体的事情: ____及时更新我的接口要求_________________

* 杜启嵘：我感谢大家对我的帮助，因为某个具体的事情：感谢大家非常支持我的工作

* 田培瑄：我感谢李国庆、韩昕睿对我的帮助，因为及时满足我对接口的需求

* 杨可清：我感谢 杜启嵘对我的帮助， 因为帮助测试与开发人员沟通，能给及时完成测试工作

* 韩昕睿：感谢四位前端同学对我的帮助，让前后端对接顺利

* 赵泽文：感谢高悠然，及时提醒我修改出的临时bug

* 李国庆：我感谢 韩昕睿对我的帮助， 因为某个具体的事情: 在我忙的帮我完成我的任务

* 石通：我感谢高悠然对我的帮助，因为我们一块开发文献管理的页面，在假期也能够很及时的交流，在开发过程中也给了我很多技术上的帮助

## 八、额外问题

1. 对比敏捷的原则，你觉得你们小组做得最好的是什么？

   * 沟通非常及时，简洁、定期反思

2. 什么是在下个阶段要改进的地方？越具体越好。

   * 采用INVEST原则拆分用户故事，新增"验收条件"字段明确定义DoD

## 九、**总结:**

1. 你觉得团队目前的状态属于 CMM/CMMI 中的哪个档次?
   * 3级，定义级
2. 你觉得团队目前处于 [萌芽/磨合/规范/创造](http://www.cnblogs.com/xinz/archive/2013/02/15/2912803.html) 阶段的哪一个阶段?
   * 创造
3. 你觉得团队在这个里程碑相比前一个里程碑有什么改进? 
   * 大家工作氛围非常愉快
4. 你觉得目前最需要改进的一个方面是什么?
   * 提高代码质量
5. 对照敏捷开发的原则, 你觉得你们小组做得最好的是哪几个原则? 请列出具体的事例。 
   * 频繁交付：每完成新功能/修复bug都进行发布，运维同学做了CI/CD
   * 欢迎变化：及时根据需求改变产品
   * 面对面交流：及时开讨论会
   * 定期反思：经常开组会进行问题讨论

正如我们前面提到的， 软件的质量 = 程序的质量 + 软件工程的质量，那团队在下一阶段应该如何提高软件工程的质量呢？

1. [代码管理的质量](http://www.cnblogs.com/xinz/p/5044037.html)具体应该如何提高？ 代码复审和代码规范的质量应该如何提高？
   * 注意代码风格和项目结构
   * 需要更多人进行代码复审，除了PM之外还需要功能相关人员进行确认
2. 整个程序的架构如何具体提高？ 如何通过重构等方法提高质量，如何衡量质量的提高？
   * 我们使用的是框架的架构
3. 其它软件工具的应用，应该如何提高？
   * 在熟悉软件工具的功能之后可以更好的使用
4. 项目管理有哪些具体的提高？
   * 通过飞书、微信、github等多平台进行项目管理
5. 项目跟踪用户数据方面，计划要提高什么地方？例如你们是如何知道每日/周活跃用户等数据的？ 
   * 进行了用户数据统计并展示在项目首页
6. 项目文档的质量如何提高？
   * 花更多时间和精力完成文档，尽量做到详实
7. 对于人的领导和管理， 有什么具体可以改进的地方？ 请看《构建之法》关于PM、绩效考核的章节， 或者 《人件》等参考书
   * PM应当提高领导力，提高与不同性格的团队成员的功能和交流能力
8. 对于软件工程的理论，规律有什么心得体会或不同意见？ 请看阅读作业。 ([这个作业的期中阅读](http://www.cnblogs.com/xinz/archive/2012/10/14/2723635.html))
   * 我们在Beta阶段中，较为良好的实践了软件工程中敏捷软工的理论

 

发布博客时，要附上全组讨论的照片。

![](https://gitee.com/du-qirong/image/raw/main/image/image-20250616130723311.png)

