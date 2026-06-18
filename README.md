# Curve Editor

基于 [CSM（可通信状态机）](https://nevstop-lab.github.io/CSM-Wiki/) 框架的曲线编辑与可视化 LabVIEW 模块。

A LabVIEW module for curve editing and visualization built on the CSM (Communicable State Machine) framework.

## 功能

- 创建、编辑和显示曲线（直线、抛物线、正弦波）
- 文件持久化（新建、打开、保存）

## 模块架构

| 文件 | 说明 |
| --- | --- |
| `Curve Editor(CSM).vi` | CSM 架构版本（当前主版本） |
| `Curve Editor(QMH).vi` | QMH 架构版本（原始版本） |
| `Curve Editor.lvlib` | 模块组（Library） |
| `Key Value.lvlib` | 支持组（Library） |
| `Curve Editor.md` | [模块接口文档](./Curve%20Editor.md) |

## 开发环境

- **LabVIEW 2020** 或更高版本
- **操作系统**：Windows

## 依赖

- [Communicable-State-Machine](https://github.com/NEVSTOP-LAB/Communicable-State-Machine)（必须）
- [CSM-API-String-Arguments-Support](https://github.com/NEVSTOP-LAB/CSM-API-String-Arguments-Support)（可选）

## 快速开始

请参阅 [Curve Editor.md](./Curve%20Editor.md) 中的完整接口文档和使用示例。

## 许可

本项目采用 Apache License 2.0 发布。详见 [`LICENSE`](./LICENSE) 和 [`NOTICE`](./NOTICE)。

## 贡献

欢迎贡献！请参阅 [`CONTRIBUTING.md`](./CONTRIBUTING.md) 了解贡献指南。

---

- _CSM Wiki：<https://nevstop-lab.github.io/CSM-Wiki/>_
- _CSM 模块仓库模板：<https://github.com/NEVSTOP-LAB/CSM-Module-Repo-Template>_
