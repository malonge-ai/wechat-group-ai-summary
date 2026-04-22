# 🚀 WeChat Group Chat AI Digest / 微信群聊AI摘要助手

* Automated AI summaries for WeChat group chats — every 5 minutes
* 每 5 分钟自动生成微信群聊 AI 摘要，并推送通知

* Turn noisy WeChat group chats into clear, structured, actionable insights.
* 将杂乱的微信群聊记录，转化为清晰、结构化、可执行的信息。


## ✨ Features / 功能亮点

* ⏱ **Auto-run every 5 minutes** / 每 5 分钟自动执行
* 📥 **Monitor QQ Mail inbox** / 监测 QQ 邮箱
* 🧠 **AI-powered summarization** / AI 自动总结
* 📊 **Structured output** / 结构化输出（概述 + 要点 + 待办）
* 📧 **Email delivery** / 邮件推送
* 💬 **WeCom notifications** / 企业微信推送
* ✅ **Skip if no new emails** / 无新邮件自动跳过

---

## 🧩 Use Case / 使用场景

**EN**

* Too many WeChat groups?
* Missing key decisions?
* Don't want to read long chat logs?

👉 This tool turns **chat chaos → actionable insights**

**中文**

* 群太多，看不过来？
* 经常错过重要信息？
* 不想翻几千条聊天记录？

👉 一键把“信息噪音”变成“关键结论”

---

## ⚙️ How It Works / 工作流程
0. 微信群聊里转发聊天记录到自己的邮箱
1. QClaw里设置一个 ⏱ 每 **5 分钟**执行一次定时任务
2. 📥 扫描 QQ 邮箱
3. 🔍 筛选邮件：

   * 发件人：`我的QQ邮箱@qq.com`
   * 标题格式：`微信群"xxx"的聊天记录`
   * 时间范围：**当天**
4. 🧠 对每封新邮件：

   * 提取聊天内容
   * AI 自动总结
   * 推送结果：
     * 📧 邮箱
     * 💬 企业微信（您的企微userid-不是中文名，一般是姓名对应的英文比如ZhangSan）
5. ✅ 若无新邮件：

   * 输出：`✅ 暂无新邮件`

---

## 🧠 AI 输出格式 / AI Output Format

### 📌 概述 / Overview（≤100字）

简要总结整体讨论内容

### 🧠 核心讨论点 / Key Points（3-5条）

* 主要讨论内容
* 关键观点/决策

### ✅ 待办事项 / Action Items（如有）

* 待执行任务
* 决策事项
* 跟进内容

---


## 🛠 使用工具 / Tools
QClaw

---

## 🛠 Prompt 配置 / Prompt Configuration
```text
设置每【5分钟】一次的定时任务 “微信群聊记录AI自动总结”。监测 QQ 邮箱中【今天】的来自 【您的QQ邮箱@qq.com】 的、标题格式为【微信群"xxx"的聊天记录】的邮件。

处理要求：
对发现的每封新邮件，用你自己的推理能力对邮件正文（chat content）进行总结，格式如下：

- 一段 100 字以内的整体概述
- 3-5 个核心讨论点（用要点列表）
- 如有待办/决策/跟进事项，单独列出

然后：
1. 使用 email-skill 发送到我的邮箱
2. 通过企业微信（openclaw-weixin）发送到【您的企微userid-ZhangSan】

如果本次没有发现新邮件：
输出「✅ 暂无新邮件」，不需要推送
```

---

## 📦 示例输出 / Example Output

```text
【群聊总结】

📌 概述：
今天群内主要围绕新品上线、库存问题及推广策略展开讨论，涉及多个角色协同。

🧠 核心讨论点：
- 新品上线时间调整至周五
- 库存不足需紧急补货
- 推广预算是否增加存在分歧
- KOL合作名单已初步确认

✅ 待办事项：
- [运营] 确认上线时间
- [供应链] 完成补货
- [市场] 确定推广预算
```

---

## 🔌 Integrations / 集成能力

* 📧 QQ Mail
* 💬 企业微信（WeCom / openclaw-weixin）
* 🧠 支持任意 LLM（OpenAI / Claude / 等）

---

## 🚀 Roadmap / 发展计划

* [ ] 多群支持（Multi-group support）
* [ ] 按话题总结（Topic-based summaries）
* [ ] 关键人物提取（Key people extraction）
* [ ] 可视化面板（Dashboard）
* [ ] SaaS 版本

---
---

## 📄 License

MIT

---

## ⭐ Star This Repo

**EN**
If this project saves you time, give it a ⭐

**中文**
如果这个项目帮你节省了时间，欢迎点个 ⭐ 支持一下
