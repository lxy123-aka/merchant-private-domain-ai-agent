# merchant-private-domain-ai-agent

基于 DeepSeek 构建的实体店私域运营 AI Agent。依托商家知识库与行业案例，支持方言意图识别、任务拆解、RAG 案例检索、营销内容生成与对话记忆，帮助实体店商家低成本开展私域运营。

## 核心功能

- **意图识别**：支持活动策划、文案生成、案例查询、策略咨询四类意图，自动提取关键信息
- **方言理解**：川渝方言正则词库 + 大模型语义兜底的双层识别
- **任务拆解**：复杂需求自动拆分为多个子任务（Plan-and-Solve）
- **RAG 检索**：向量检索 + Cross-Encoder 重排，精准匹配行业案例
- **内容生成**：朋友圈文案、活动方案、到店话术，可直接使用
- **对话记忆**：跨会话记住商家信息，无需重复描述



## 项目结构

```
├── app.py                  # 前端入口
├── agent/
│   ├── core.py             # Agent 核心调度
│   ├── intent.py           # 意图识别
│   ├── task_planner.py     # 任务拆解
│   └── prompt_builder.py   # Prompt 组装
├── memory/
│   └── memory_module.py    # 对话记忆管理
├── rag/
│   └── search.py           # RAG 检索
├── data/
│   ├── cases/              # 案例库
│   └── dialect/            # 方言词库
└── utils/
    └── filter.py           # 敏感词过滤

```

