# 四家 AI 的"会员 vs API"对照速查：ChatGPT、Claude、Gemini、Grok

> **最后核验：2026-10-01** · 维护方：MuyuGPT（[muyugpt.com](https://muyugpt.com/)）
>
> **第三方身份说明：** MuyuGPT 是独立第三方 AI 订阅指南与订阅协助平台，与 OpenAI、Anthropic、Google、xAI 不存在官方隶属、授权或合作关系。
>
> **把握程度：** 表里每一格都标了来源等级：**官方**＝来自该公司页面的公开内容；**整理**＝多家公开整理一致但未能在官方页面逐字核实；**未确认**＝没有可靠依据。OpenAI 和 xAI 的官方页面对自动读取设置了限制，本文未绕过。

## 一句话

**四家都是一样的：个人订阅（会员）和开发者 API 是两套独立账户、两套计费，互不抵扣。** 买了会员不会给你 API 额度，给 API 充值也不会增加会员用量。

## 对照表

| | ChatGPT（OpenAI） | Claude（Anthropic） | Gemini（Google） | Grok（xAI） |
| --- | --- | --- | --- | --- |
| 会员叫什么 | Plus、Pro（100 / 200 / 500） | Pro、Max（5x / 20x） | Google AI Plus / Pro / Ultra（5x / 20x） | SuperGrok（档位名称以官方为准） |
| 会员含 API 吗 | 不含（整理） | 不含，Max 也不含（官方） | 不含（整理） | 不含（整理） |
| API 在哪里管理 | OpenAI 开发者平台 | Claude Console（控制台） | Google AI Studio / Google Cloud | xAI 开发者控制台 |
| API 怎么收费 | 按量 | 预付额度，按 token | 有免费层，超出按付费价格（整理） | 按 token（整理） |
| 会员里的"额外用量" | credits（用于 Codex、ChatGPT Work 等） | usage credits，按标准 API 价格（官方） | AI Studio 更高限额、每月 Google Cloud 额度（官方方案页） | 未确认 |
| 编程工具 | Codex：包含在各套餐（含 Free、Go），云端环境需 Plus+（官方） | Claude Code：包含在所有付费档（官方） | Antigravity、Jules 等（官方方案页，限额随档位） | 未确认 |

## 编程工具的"两种登录方式"

| | 用会员账号登录 | 用 API 密钥登录 |
| --- | --- | --- |
| Codex | 走 ChatGPT 套餐额度，有云端功能（官方） | 按开发者平台标准价格计费，无云端功能（官方） |
| Claude Code | 走 Pro / Max 订阅用量（官方） | 按 token 计费，使用控制台账户（官方） |

**共同的坑：** 环境变量里放着 API 密钥（如 `ANTHROPIC_API_KEY`、`OPENAI_API_KEY`）时，工具可能优先走 API 计费。用各工具的状态命令（如 `/status`）确认当前生效的是哪种登录方式。

## 取消订阅的基础

| | ChatGPT | Claude | Gemini | Grok |
| --- | --- | --- | --- | --- |
| 在哪里取消 | ChatGPT 的计划设置（网页）；应用商店订阅到商店里取消 | Settings → Billing → Cancel；Android 在 Billing → Manage subscription；iPhone 到 Apple 取消（官方） | Google 账号 / Google One 的订阅管理 | 网页订阅在账号设置；应用商店订阅到商店里取消（整理） |
| 何时生效 | 以账号显示为准 | 当前计费周期结束；官方建议提前 24 小时（官方） | 以订阅管理页面显示为准 | 整理：周期结束前仍可使用 |
| 取消会停 API 吗 | 不会（两套独立） | 不会（官方） | 不会（两套独立） | 不会（整理） |

## 怎么用这张表

1. **先问自己在干什么**：自己用 → 会员；给程序用 → API；编程工具两者都行，但要知道当前用的是哪种登录方式。
2. **买之前核对**：档位名称、计费周期、含不含税、是会员还是 API。
3. **买之后核对**：到账号的订阅页确认档位和到期日，到用量或账单页确认有没有意外的 API 费用。
4. 各家的细节手册：[ChatGPT Pro 套餐手册](https://github.com/muyugpt-official/gpt-chongzhi/blob/main/chatgpt-pro-tiers-2026.md)、[Claude 套餐与用量限制](https://github.com/muyugpt-official/claude-chongzhi/blob/main/docs/claude-plans-and-limits-2026.md)、[Claude Code 登录与计费](https://github.com/muyugpt-official/claude-chongzhi/blob/main/docs/claude-code-login-and-billing.md)、[Google AI 套餐手册](https://github.com/muyugpt-official/gemini-chongzhi/blob/main/docs/google-ai-plans-2026.md)、[Gemini 订阅与 API](https://github.com/muyugpt-official/gemini-chongzhi/blob/main/docs/gemini-subscription-vs-api.md)、[SuperGrok 套餐名称与核对方法](https://github.com/muyugpt-official/grok-chongzhi/blob/main/docs/supergrok-plan-names-and-how-to-verify.md)。

## 常见问题

### 四家里哪家的会员含 API？
没有。四家都把会员和 API 分开计费。

### 我买了会员，为什么还有 API 账单？
最常见的原因是环境变量里的 API 密钥让编程工具优先走了 API，或者你同意了"用量用完后改用 API 额度"的选项。先看状态命令显示的登录方式。

### 取消会员，API 会停吗？
不会。要到各自的开发者控制台单独处理。

### 这张表里的"整理"是什么意思？
多家公开整理一致，但我们没能在官方页面逐字核实的说法。下单或做决定前，请以官方页面为准。

## 相关阅读

- [价格与政策变更记录](./价格与政策变更记录.md)
- [官方帮助中心链接索引](./官方帮助中心链接索引.md)
- [返回知识库首页](../../README.md)

> MuyuGPT 是独立第三方 AI 订阅指南与订阅协助平台，与 OpenAI、Anthropic、Google、xAI 不存在官方隶属、授权或合作关系。
