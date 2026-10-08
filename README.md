# 用 AI 把手上的活重做一遍

> 财务出身，2027 届应届生。
> 这里放的不是作业，是我自己在用的东西——台账要核对、周报要做、岗位要筛，
> 做完就留下来，能跑就用。
>
> 判断标准只有一条：**有没有真的省下时间**。

---

## 先说结论

| 做了什么 | 原来 | 现在 |
|---|---|---|
| 财务台账异常核对 | 5 小时 / 批 | 2 小时 / 批 |
| 团队周报 PPT（约 30 页） | 手工逐页填 | 8 步流程跑完，格式零改动 |
| 秋招岗位筛选 | 逐个看 JD | 抓岗位 → AI 评分 → Excel 清单，成批出 |

数字来自实际使用，不是估算。

---

## 仓库索引

| 仓库 | 是什么 | 技术栈 |
|---|---|---|
| [finance-tools](https://github.com/lucascxxc/finance-tools) | 财务台账异常检测 + 财报分析生成器 | 单文件 HTML |
| [job-search-kit](https://github.com/lucascxxc/job-search-kit) | 秋招工作流脚本：抓岗位到出清单 | Python |
| [wechat-bill-stats](https://github.com/lucascxxc/wechat-bill-stats) | 说句话就记账的微信账单助手 | TypeScript 全栈 |
| [ai-screenshot-assistant](https://github.com/lucascxxc/ai-screenshot-assistant) | 截图即问 AI 的桌面工具 | Python |
| [workbuddy-skills](https://github.com/lucascxxc/workbuddy-skills) | 沉淀成 Skill 的可复用流程 | Skill 定义 + Python |
| [web-apps](https://github.com/lucascxxc/web-apps) | 单文件网页作品 | HTML |

---

## 重点作品

挑了三件最能说明「怎么用 AI 干活」的，各写了一份拆解：

### 1. [财务台账异常检测 · 完整拆解](showcase/01-财务台账异常检测.md)
单文件 HTML，双击就跑，数据不出本地。把核对规则写成代码，
人只负责看结果做判断。**从 5 小时压到 2 小时的关键不在 AI，在把规则显式化。**

### 2. [周报自动化 · 完整拆解](showcase/02-周报自动化.md)
约 30 页 PPT，8 步流程，三条铁律写进代码：
同项目按编号更新、没提到的原样保留、图表版式字体涉密内容一律不动。
**难的不是生成内容，是「不动」那些不该动的东西。**

### 3. [AI 截图助手 · 完整拆解](showcase/03-AI截图助手.md)
Python 桌面工具，常驻托盘，全局热键截图直接问 AI，结果能同步到手机。
支持多家模型，也支持本机 Ollama 完全离线。

---

## 一点方法论

[用 AI 重做手上的活儿：几条踩出来的经验](tips/用AI重做手上的活儿.md)

不是 prompt 技巧，是**哪些活儿值得重做、怎么判断做完没做完**。

---

## 关于数据

- 所有工具默认**不联网**、数据不出本地（除非明确调用模型 API）
- 密钥一律走 `.env` / `config.ini`，仓库里只放值已清空的 `.example` 模板
- 涉密内容不进任何仓库
