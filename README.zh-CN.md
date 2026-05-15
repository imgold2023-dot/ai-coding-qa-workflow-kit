# AI Coding QA Workflow Kit 简体中文说明

这是一个面向独立开发者、QA 工程师和小型技术团队的公开资源入口，适合正在使用 AI 编程工具的人。

它的目标是：在你让 AI 写测试之前，先把工具安全、需求、验收标准、测试矩阵和 Playwright 自动化计划拆清楚。

## 从这里开始

免费资源：

- [AI 编程工具安全门槛清单](./AI-Coding-Tool-Safety-Gate-Checklist.zh-CN.md)

预览：

- [PRD to Playwright QA Starter Pack 预览](./prd-to-playwright-preview.zh-CN.md)

状态：

- 完整包暂时不可购买，收款通道调整完成后再重新开放。

## 为什么做这个

AI 编程工具可以很快写 PRD、测试用例和 Playwright 脚本。

问题是：速度会掩盖很多弱假设：

- 产品范围模糊
- 验收标准缺失
- selector 脆弱
- 测试数据不安全
- 过度相信 AI 生成代码
- 太早使用真实凭证或生产数据

这个 repo 关注的是自动化之前的工作流：

```text
粗略功能想法
  -> PRD 澄清
  -> 验收标准
  -> 风险发现
  -> 测试用例矩阵
  -> 测试数据策略
  -> Playwright 自动化计划
  -> 测试代码审查
  -> 发布前冒烟检查
```

## 免费清单

在你安装、运行、连接或信任这些内容前，先过一遍清单：

- AI 编程工具
- GitHub repo
- agent workflow
- MCP server
- 浏览器自动化脚本
- 第三方模板

判断标签：

- `Use`
- `Use with isolation`
- `Study only`
- `Reject`

## 完整包

`PRD to Playwright QA Starter Pack` 包含：

- 10 个串联 prompt
- 5 个可复用模板
- 1 个虚构 SaaS 功能完整示例
- 英文和简体中文 README

当前状态：暂时下架，等待稳定收款通道确认后重新开放。

## 安全边界

不要把真实客户数据、生产 token、cookie、浏览器配置、银行卡、支付账号凭证或敏感信息粘贴到任何 AI 工具里。

先用假数据、沙盒环境和人工审查。

这个 repo 不保证绝对安全、不保证软件无 bug，也不替代生产级自动化评审。它是一个实用起点。
