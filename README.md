# Game PRD Analyzer

游戏策划需求解析器 · 交互设计师专用

## 在线访问

https://21bae4a7cd9a4282990fccf6813a563d.app.codebuddy.work

## 功能

- **多格式文档输入**：TXT / MD / DOCX / Excel（xlsx/xls）
- **Excel 内嵌图片自动提取**：自动解包 Excel 中的流程图、界面草图、示意图
- **图片上传**：支持单独上传流程图/界面草图
- **9 步固定结构分析**：严格按交互设计标准输出
- **AI 模型自由选择**：支持 OpenAI / Anthropic / Google / 阿里云 / Moonshot / DeepSeek / SiliconFlow / 自定义
- **Prompt 一键复制**：不填 API Key 也能复制完整 Prompt 到其他 AI 使用
- **结果导出**：Markdown / DOCX
- **本地历史记录**：浏览器本地保存，不上传数据

## 支持的 AI 模型

| 服务商 | 模型示例 | 视觉 |
|--------|---------|------|
| Anthropic | Claude Opus 4.3 / Sonnet 4 / Haiku 4 / Sonnet 3.5 | ✅ |
| OpenAI | GPT-5.5 / GPT-4.1 / GPT-4o / o1 / o3-mini | 部分 ✅ |
| Google | Gemini 2.5 Pro / 2.0 Flash / 1.5 Pro | ✅ |
| 阿里云 | Qwen-VL-Max / Qwen2.5-VL / Qwen-Max | 部分 ✅ |
| Moonshot | Kimi k1.5 / K2 | ❌ |
| DeepSeek | DeepSeek-V3 / R1 | ❌ |
| SiliconFlow | DeepSeek-V3 / R1 / Qwen2.5-VL | 部分 ✅ |
| 自定义 | OpenAI 兼容接口 | 视模型而定 |

> 模型选择不预设默认值，必须手动选择，避免低等级模型导致分析不明确。

## 9 步分析结构

1. 核心设计目标梳理
2. 功能主干流程
3. 全部界面清单
4. 全界面状态枚举
5. 用户操作行为清单
6. 跳转逻辑与页面关系
7. 边界异常场景枚举
8. 需求缺陷与待确认清单
9. 交互设计工作量前置评估

## 使用建议

- 含图片/流程图的 Excel：优先选 Claude Opus 4.3 / GPT-5.5 / Gemini 2.5 Pro / Qwen-VL-Max
- 纯文字长 PRD：可选 DeepSeek-V3 / Kimi k1.5，性价比高
- 复杂系统深度拆解：首选 Claude Opus 4.3 / GPT-5.5 / o1

## 数据安全

- API Key 仅存在浏览器 `localStorage`，不会上传到服务器
- 分析请求直接发向你选择的 AI 服务商
- 历史记录仅保存本地

## 文件位置

- 源码：`tools/prd-analyzer/index.html`
- 说明：`tools/prd-analyzer/README.md`
