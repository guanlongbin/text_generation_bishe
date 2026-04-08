# EvoGenAgents 测试用例生成系统

## 简介

基于多智能体协作的自动化测试用例生成系统，通过规划智能体、工具智能体、生成智能体和反思智能体的协作，将需求文档自动转化为测试用例。

## 系统架构

```
原始需求文档 → 规划智能体(中心协调)
                    ↓
            工具智能体(实体识别/检索)
                    ↓
            规则记忆(业务规则库)
                    ↓
            生成智能体(案例生成)
                    ↓
            反思智能体(质量评估) ↔ 规划智能体
                    ↓
                  输出(测试案例)
```

### 核心智能体

- **规划智能体**: 任务拆解与流程协调
- **工具智能体**: 实体识别与信息检索
- **规则记忆**: 业务规则库存储与查询
- **生成智能体**: 测试用例生成
- **反思智能体**: 质量评估与反馈优化

## 项目结构

```
├── index.html              # 首页导航
├── pages/
│   ├── dashboard.html     # 控制面板
│   ├── agents.html         # 多智能体框架可视化
│   ├── generation.html    # 测试用例生成
│   ├── entity-extraction.html  # 实体抽取
│   ├── preprocess.html     # 预处理
│   └── vectordb.html       # 向量数据库
└── *.docx/*.xlsx           # 需求文档
```

## 运行方式

### 方式一：Python HTTP 服务器

```bash
cd /Users/guanyalong/Documents/trae_projects
python -m http.server 8000
```

访问: http://localhost:8000

### 方式二：Node.js HTTP 服务器

```bash
cd /Users/guanyalong/Documents/trae_projects
npx serve -p 8000
```

### 方式三：VS Code Live Server

使用 VS Code 插件 Live Server，右键点击 index.html 选择 "Open with Live Server"

## 依赖

- 无需安装任何依赖
- 仅使用 CDN 加载的库：Tailwind CSS, Lucide Icons
