# TestGuard（验收测试防护）

> 本 wrapper 尚未接入独立引擎；`check` 固定返回 `DESIGN_ONLY`、退出码3，不会调用引擎或产生通过证据。独立引擎的已有功能不等于本插件已可执行。

**版本**：0.1.1 · **许可证**：Apache-2.0 · **技能**：1 个

[English](README.en.md)

## 项目定位

TestGuard 是 Partme Guard 研发防护体系中的独立插件，命令前缀为 testguard。它不依赖统一总命令，可独立安装、独立发版、独立执行。

## CLI 命令

| 命令 | 类型 |
| :--- | :--- |
| version | 独立入口 |
| doctor | 独立入口 |
| status | 独立入口 |
| discover | 独立入口 |
| check | 独立入口 |
| init | 独立入口 |

## 安装

在 [Full Stack Plugins 市场](https://github.com/partme-ai/full-stack-plugins) 中选择插件 ID `testguard`。仓库名 `testguard-plugin` 与插件 ID 不同。当前固定安装版本为 `v0.1.1`；宿主安装是否自动将 `bin/` 加入 PATH 需按宿主验证。

## 快速开始

~~~bash
testguard version
testguard doctor
testguard status
~~~

## 当前状态

本 wrapper 尚未接入独立引擎；`check` 固定返回 `DESIGN_ONLY`、退出码3，不会调用引擎或产生通过证据。独立引擎的已有功能不等于本插件已可执行。

没有真实执行证据时，不报告 PASS；未实现能力报告 DESIGN_ONLY 或 UNVERIFIED。

## 架构

命令入口、生命周期、只读检查和证据边界见 product-docs/TestGuard/ 与 docs/。

## 边界

- 不合并为 Partme Guard 总命令。
- 不替代其他 Guard 的专业判断。
- 不自动提交、推送或修改用户代码。

## 验证

~~~bash
sh bin/testguard version
# Expected: DESIGN_ONLY and exit code 3
sh bin/testguard check
~~~

## 许可证

Apache-2.0
