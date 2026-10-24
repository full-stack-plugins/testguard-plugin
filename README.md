# TestGuard（验收测试防护）

> 冻结测试计划、归一化原生执行证据、识别删测跳测与覆盖缺口。

版本：0.1.0 · 许可证：Apache-2.0

## 定位

验证必需行为是否真的被执行，而不是只看退出码。

当前为插件脚手架：有真实 CLI 时执行并保留证据；无 CLI 时明确输出 DESIGN_ONLY，不冒充通过。

## 安装

codex plugin marketplace add partme-ai/full-stack-plugins
codex plugin add testguard@full-stack-plugins

## 边界

- 不替代其他专业 Guard。
- 不绕过受保护分支、必需检查或人工审批。
