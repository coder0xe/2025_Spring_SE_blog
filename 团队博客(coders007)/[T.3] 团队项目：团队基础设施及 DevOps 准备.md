# [T.3] 团队项目：团队基础设施及 DevOps 准备

| 项目                                 | 内容                                                         |
| ------------------------------------ | ------------------------------------------------------------ |
| 这个作业属于哪个课程                 | [2025年春季软件工程（罗杰、任健）](https://edu.cnblogs.com/campus/buaa/BUAA_SE_2025_LR) |
| 这个作业的要求在哪里                 | [[T.3] 团队项目：团队基础设施及 DevOps 准备](https://edu.cnblogs.com/campus/buaa/BUAA_SE_2025_LR/homework/13396) |
| 我在这个课程的目标是                 | 提升软件工程化能力，提升团队合作与交流沟通能力，培养敏捷开发能力 |
| 这个作业在哪个具体方面帮助我实现目标 | 配置团队开发基础设施，提高后续开发效率                       |

## 服务器选择

基于我们的在线文献学习平台jieNote的需求，我们选择了腾讯云的两台服务器进行配置：

### 1.主应用服务器

**厂商**: 腾讯云

| 配置项   | 选择内容            | 选择原因                               |
| -------- | ------------------- | -------------------------------------- |
| 地域     | 北京                | 离用户群体近，延迟低                   |
| 计费方式 | 包年包月            | 项目周期约3个月，包年包月更经济        |
| CPU      | 2核                 | 满足应用服务基本计算需求               |
| 内存     | 8G                  | 考虑文献处理、笔记编辑等内存密集型操作 |
| 公网带宽 | 7M                  | 平衡成本与用户体验                     |
| 系统盘   | 高性能云硬盘SSD 80G | 确保系统运行流畅                       |
| 数据盘   | 无                  | 采用COS对象存储服务器                  |

综合考虑：

- 2核8G配置能够满足我们Alpha和Beta阶段的应用需求
- 8G内存特别考虑了文献批注和笔记编辑时可能的内存需求
- 7M带宽足以支持初期用户访问量
- 成本与性能的权衡

### 2.COS对象存储服务器

**厂商**: 腾讯云COS

| 配置项   | 选择内容         |
| -------- | ---------------- |
| 地域     | 北京             |
| 存储类型 | 标准存储         |
| 存储容量 | 100G             |
| 计费方式 | 超量部分按量收费 |

综合考虑：

- 专门用于存储用户上传的文献和笔记附件

- 与主应用服务器分离，实现数据服务分离
- 主服务器专注于应用逻辑处理，COS服务器专注于文献和笔记的存储，实现职责分离
- 减轻主服务器的I/O压力，利用COS的专业存储服务提高文件存取效率

## 团队管理

### 团队沟通、协助

我们团队选择使用 **飞书（Feishu）** 作为主要的沟通平台。
 具体使用方式如下：

- **日常交流**：通过飞书的即时消息功能进行团队成员之间的快速沟通，方便讨论项目进展和技术细节；
- **在线会议**：遇到复杂问题或需要多成员参与讨论时，使用飞书的会议功能进行讨论；
- **公告与任务同步**：通过飞书的群公告、日历、待办事项功能同步项目进度、重要事项和会议安排；
- **文档共享**：使用飞书自带的文档功能（类似在线Office），快速共享需求、方案、会议纪要等内容。

飞书集成性强，能够把沟通、文档、日程等集中到一个平台中，提升效率。

### 代码管理

我们选择**GitHub**进行代码管理。

- **分支管理**：采用 feature 分支开发流程，每个功能点由一名或多名开发者在独立分支上完成；

- **Pull Request（PR）协作**：开发完成后提交 PR，由其他成员代码审查后合并；

- **Issue管理**：在 GitHub 上开设 Issue 跟踪 Bug 和任务；

- **项目看板（Project Board）**：可选用 GitHub 自带看板做任务流管理（与飞书看板可互补使用）；

- **CI/CD**：配置 GitHub Actions 实现自动构建、测试和部署流程，提高开发效率与稳定性。

## CI/CD

### 配置文件

```
name: Build and Deploy Hugo

on:
  push:
    branches:
      - main

jobs:
  build-deploy:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v4
      with:
        submodules: recursive
    - name: Initialize submodules
      run: git submodule update --init --recursive
    - name: Setup Hugo
      uses: peaceiris/actions-hugo@v2
      with:
        hugo-version: 'latest'
    - name: Build
      run: hugo --minify
    - name: Disable Jekyll
      run: touch public/.nojekyll
    - name: Deploy to GitHub Pages
      uses: peaceiris/actions-gh-pages@v3
      with:
        github_token: ${{ secrets.GITHUB_TOKEN }}
        publish_dir: ./public
```

### 触发截图

![CICD触发](https://gitee.com/tian-peixuan/imgs/raw/master/CICD触发.png)
