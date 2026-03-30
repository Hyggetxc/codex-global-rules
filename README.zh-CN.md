# codex-global-rules

> 用一个地方统一管理 Codex 全局规则，方便跨项目复用、备份和同步。

[![GitHub Stars](https://img.shields.io/github/stars/Hyggetxc/codex-global-rules?style=flat-square)](https://github.com/Hyggetxc/codex-global-rules/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/Hyggetxc/codex-global-rules?style=flat-square)](https://github.com/Hyggetxc/codex-global-rules/network/members)
[![GitHub Issues](https://img.shields.io/github/issues/Hyggetxc/codex-global-rules?style=flat-square)](https://github.com/Hyggetxc/codex-global-rules/issues)
[![AGENTS.md](https://img.shields.io/badge/AGENTS-md-2f81f7?style=flat-square)](https://github.com/Hyggetxc/codex-global-rules/blob/main/AGENTS.md)

`codex-global-rules` 是一个用于集中维护 Codex 全局规则的仓库。

它适合下面这些场景：

- 希望把跨项目复用的 Codex 规则统一维护在一个地方
- 想把可复用的 `AGENTS.md` 在不同设备或工作区之间同步
- 希望给重要规则变更加上快照留档
- 希望公开发布规则时，默认脱敏，不暴露真实本地设备名和项目名

## 语言

- [English](./README.md)
- [简体中文](./README.zh-CN.md)

## 在线地址

- 仓库地址：[https://github.com/Hyggetxc/codex-global-rules](https://github.com/Hyggetxc/codex-global-rules)
- 主规则文件：[AGENTS.md](https://github.com/Hyggetxc/codex-global-rules/blob/main/AGENTS.md)

## 这个仓库解决什么问题

当 Codex 在多个项目里长期使用时，协作规则很容易慢慢分散、失真，最后变成：

- 不同项目规则不一致
- 旧规则没有版本留档
- 新设备不知道以哪份规则为准
- 公开共享时容易把本地路径、设备名或敏感项目名一起提交出去

这个仓库的作用就是把全局规则集中收口到一个版本化入口里，方便统一维护、备份、同步和复用。

## 功能特性

- 用 `AGENTS.md` 作为全局规则主文件
- 用 `snapshots/` 保存重要规则变更的快照
- 使用 `<用户目录>` 这类占位写法，避免提交真实本地路径
- 默认避免提交真实设备名、用户名和敏感项目名
- 适合作为长期维护的 Codex 全局协作规则仓库

## 仓库结构

- `AGENTS.md`：全局规则主文件
- `snapshots/`：规则快照与留档说明目录

## 使用方式

1. 先阅读仓库里的 [`AGENTS.md`](./AGENTS.md)
2. 按自己的协作方式做必要调整
3. 同步到 Codex 用户级全局规则路径
4. 大改之前先保存快照
5. 再把更新推回这个仓库，作为统一来源

示例用户级路径：

- Windows：`%USERPROFILE%\\.codex\\AGENTS.md`

实际使用时请替换为你自己的本地用户目录，不要把真实机器路径反向提交回仓库。

## 隐私说明

- 这个仓库只建议保存脱敏后的全局规则
- 不应提交真实本地设备名、真实用户名和真实项目名
- 路径、目录和设备信息尽量使用 `<用户目录>`、`<当前项目>` 这类通用占位

## Roadmap

后续很适合继续扩展：

- `docs/`：放安装指南、同步说明、示例
- 更多双语文档
- 按场景拆分的规则模板
- 重大规则版本的 release notes
- 项目级继承与覆盖的示例说明

## 支持一下

如果这个仓库帮你更稳定地管理和复用 Codex 全局规则，欢迎给它点个 Star：

- [给这个仓库点个 Star](https://github.com/Hyggetxc/codex-global-rules)
