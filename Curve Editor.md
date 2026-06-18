# `Curve Editor` — CSM 模块接口文档

---

## 功能简述

`Curve Editor` 是一个 CSM 模块，用于创建、编辑和显示曲线（直线、抛物线、正弦波）。支持曲线定义文件的新建、修改和保存。

---

## 模块信息

| 属性           | 值                                              |
| -------------- | ----------------------------------------------- |
| LabVIEW 版本   | ≥ 2020                                          |
| 支持的操作系统 | Windows                                         |
| 支持 RT        | ❌ 不支持                                       |
| 支持 64-bit    | ✅ 支持                                         |
| 所属模块组     | Curve Editor.lvlib                              |

---

## 依赖项

| 依赖                                                                                                | 类型 |
| --------------------------------------------------------------------------------------------------- | ---- |
| [Communicable-State-Machine](https://github.com/NEVSTOP-LAB/Communicable-State-Machine)             | 必须 |
| [CSM-API-String-Arguments-Support](https://github.com/NEVSTOP-LAB/CSM-API-String-Arguments-Support) | 可选 |

---

## API 接口（消息接口）

以下是外部调用者可以发送给本模块的消息。

### `API: Open File`

打开曲线文件。当已有文件打开时，会丢弃其修改并直接打开文件。

- **参数**：`APIString` — `String`：曲线文件路径
- **响应**：N/A

### `UI: Front Panel State`

控制本模块前面板的显示状态。

- **参数**：`APIString` — `Enum`：`Open`、`Close` 或 `Minimize`
- **响应**：N/A

### `UI: Cursor Set`

设置前面板光标样式。

- **参数**：`APIString` — `Enum`：光标类型名称（如 `Busy`、`Default`）
- **响应**：N/A

### 参数类型说明

| 类型        | 说明                                                                                              |
| ----------- | ------------------------------------------------------------------------------------------------- |
| `APIString` | 支持嵌套键值对的纯文本字符串，需要 CSM API String Arguments Support 插件                          |

## 调用限制与注意事项

> [!IMPORTANT]
>
> - 本模块为**单例**——同一时间不可运行多个实例。

---

## 使用示例

### 基本生命周期

1. 启动后创建一个新文件或打开一个已有文件

2. 添加或编辑一组曲线

3. 保存文件

---

## 备注

- 本模块由 QMH（队列消息处理器）架构重构为 CSM 架构，`Curve Editor(QMH).vi` 为原始版本，`Curve Editor(CSM).vi` 为 CSM 版本。
- 如需修改本模块中曲线组件的图标，可以替换Pitures文件夹下的图片文件，图片大小为16x16，格式为PNG。。
- 键值对数据管理使用 `Key Value.lvlib` 子模块可独立使用。

---

- _完整 CSM 语法参考：<https://github.com/NEVSTOP-LAB/Communicable-State-Machine/blob/main/.doc/Syntax.md>_
- _CSM Wiki：<https://nevstop-lab.github.io/CSM-Wiki/>_
- _CSM 模块仓库模板：<https://github.com/NEVSTOP-LAB/CSM-Module-Repo-Template>_
