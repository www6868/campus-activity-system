# 校园活动报名与签到管理系统 — 实验总结报告

## 1. 项目概述
本项目用于《软件项目管理》课程综合实验，在统一题目“校园活动报名与签到管理系统”背景下完成项目初始化、WBS分解、简化进度计划、配置管理与协作提交。

## 2. 团队成员与角色
| 姓名（拼音） | 角色 | 主要职责 |
|---|---|---|
| wangjiaming | 项目经理 | 统筹进度、仓库管理、最终合并main、参与冲突制造 |
| yuyawen | 计划负责人 | 负责WBS与进度计划文档（02-wbs.md、03-schedule.md） |
| liyouran | 配置管理员 | 仓库、分支管理、配置管理文档（04-configuration.md）、解决合并冲突 |
| jianzhixin | 协作成员 | 参与文档完善、分支提交、与wangjiaming制造冲突 |

## 3. 项目目录结构
.
├── README.md
├── docs
│ ├── 02-wbs.md
│ ├── 03-schedule.md
│ ├── 04-configuration.md
│ ├── 05-summary-report.md
│ └── conflict.md
├── src
├── test
└── assets

text

## 4. 分支约定
- `main`：最终提交分支，受保护
- `dev`：开发集成主分支
- `feature/*`：各成员/功能分支（如 feature/conflict-wang、feature/conflict-jian 等）

## 5. 实验完成情况
- [x] 项目初始化与README完成
- [x] WBS三级分解完成（围绕交付物，见02-wbs.md）
- [x] 简化进度计划形成（明确前置关系、工期、责任人，见03-schedule.md）
- [x] 配置项识别与分支策略制定（见04-configuration.md）
- [x] 冲突制造与解决：由wangjiaming与jianzhixin分别修改docs/conflict.md同一位置，合并时产生冲突，由配置管理员liyouran手工解决
- [x] 总结报告合并至main（已完成）

## 6. 冲突解决过程
- **制造方式**：wangjiaming在feature/conflict-wang分支将docs/conflict.md修改为“系统应支持线下扫二维码签到”；jianzhixin在feature/conflict-jian分支将同一文件同一行修改为“系统应支持手动输入学号和扫描二维码两种签到方式”。
- **冲突产生**：liyouran将feature/conflict-wang合并到dev后，再合并feature/conflict-jian时触发内容冲突。
- **解决方案**：手动编辑docs/conflict.md，删除Git冲突标记，综合双方内容为“系统应支持线下扫二维码签到及手动输入学号两种方式”，随后提交并推送至dev。

## 7. 实验收获
- 掌握了基于Git的团队协作流程，包括分支创建、合并、冲突解决。
- 理解了以交付物为导向的WBS分解方法，能够围绕文档、模块原型等工作成果进行规划。
- 实践了配置管理的基本要素：识别配置项、制定分支策略、权限与合并规则。
- 认识到前置沟通、提交规范对协作效率的重要性。