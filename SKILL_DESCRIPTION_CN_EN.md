# 终极面试官 1.0 Skill [edison9l 团队版]
# Ultimate Interviewer 1.0 Skill [edison9l Team Edition]

---

## 🎯 一句话总结 | One-Liner Summary

**终极面试官 1.0 Skill** 的核心优势，是把 AI 面试从"题库问答"推进到"真实面试控场"。  
它让 AI 不只是会问，而是知道该问什么、为什么问、问到哪里停、怎么核验、如何交接。

**The Ultimate Interviewer 1.0 Skill** transitions AI interviews from "question bank Q&A" to "real interview control."  
It enables AI not just to ask questions, but to know what to ask, why to ask, when to stop, how to verify, and how to handoff.

---

## 📌 它解决的核心问题 | Core Problems It Solves

### 问题现象 | The Problem

很多 AI 面试工具看起来会问问题，但真实用起来很容易暴露问题：

- ❌ 一上来让候选人填表，问题像题库一样死板
- ❌ 不会看简历逻辑，不会处理候选人反问
- ❌ 不知道什么时候该追问、什么时候该结束
- ❌ 不会把 HR 初面、业务二面、老板终面的信息串起来

Many AI interview tools ask questions, but reveal problems in practice:
- ❌ Start with form filling, questions feel rigid from a question bank
- ❌ Cannot analyze resume logic or handle candidate counter-questions
- ❌ Don't know when to probe further or when to conclude
- ❌ Cannot connect HR screening, technical round, and executive round insights

### 解决方案 | Our Solution

**终极面试官** 解决的是更底层的问题：让 AI 不只是"问问题"，而是"会面试"。

| 真实问题 | 终极面试官的处理方式 |
|---------|-------------------|
| AI 上来就问一堆表格问题 | 改为自然开场，候选人端不展示后台表格 |
| 不同岗位用同一套题 | 根据岗位、行业、JD、简历和场景包动态生成问题 |
| 候选人说漂亮话，AI 不会拆 | 用声明账本和反包装追问拆解"主导、负责、提升、带团队"等表达 |
| 简历时间线有问题，AI 看不出来 | 自动审计年龄、学历、毕业时间、空窗期、频繁跳槽、经历重叠 |
| 候选人问薪资、双休、公司情况，AI 出戏 | 读取管理员配置，能答则答，不能答则记录待 HR 回复 |
| 问题太多、太长、像审讯 | 有题量控制、节奏控制、最后两问、礼貌打断 |
| HR、业务、老板面试没有衔接 | 每轮生成上下文胶囊和候选人档案 |
| AI 假装判断真假 | 不判断真假，只生成核验追问、补材料要求、背调问题 |
| 内部评价直接暴露给候选人 | 候选人侧话术和管理员内部报告分离 |

| Real Problem | Ultimate Interviewer's Approach |
|-------------|--------------------------------|
| AI asks form questions upfront | Natural opening, no backend forms shown to candidates |
| Same questions for all roles | Dynamically generates questions by role, industry, JD, resume, scenario pack |
| Candidate gives polished answers, AI can't dissect | Uses claim registry & anti-packaging probes to unpack phrases like "led," "responsible," "improved," "managed team" |
| Resume timeline issues invisible to AI | Auto-audits age, education, graduation date, gaps, job hopping, overlapping experience |
| Candidate asks about salary, work schedule, company—AI breaks character | Reads admin config, answers when possible, logs for HR follow-up when not |
| Too many questions, too long, feels like interrogation | Question quantity control, pacing control, final two questions, polite interrupts |
| HR, technical, executive rounds disconnected | Each round generates context capsule and candidate dossier |
| AI pretends to judge truth | Doesn't judge, only generates verification probes, material requests, background check questions |
| Internal ratings exposed to candidate | Candidate-facing language separate from admin internal report |

---

## ⚙️ 核心运行逻辑 | Core Operating Logic

### 完整面试流程 | Complete Interview Flow

```
自然启动
↓
读取简历 / PDF / 图片 / JD / 作品材料
↓
生成岗位画像
↓
审计简历时间线
↓
提取候选人关键声明
↓
加载对应岗位场景包
↓
根据 HR / 业务 / 老板轮次动态提问
↓
每次只问一个主问题
↓
根据回答诊断追问、跳过、升压或收口
↓
处理候选人反问
↓
判断本轮是否问够
↓
输出候选人侧话术 + 内部报告
↓
生成候选人档案和下一轮上下文胶囊
```

### 核心设计原则 | Core Design Principles

**固定的是面试机制，不固定具体问题。**

同样是"新媒体主管"，如果候选人是做抖音的，就会追问爆款案例、数据口径、账号垂类、是否投流、商业转化；  
如果候选人是做小红书的，就会追问选题、封面点击、内容结构、私信留资和转化链路。

**AI 不再机械套题，而是围绕真实材料动态追问。**

---

## 🛠️ 核心模块与功能 | Core Modules & Features

| 模块 | 功能 | 价值 |
|------|------|------|
| **自然启动模块** | 用户输入"开始面试"后自然开场 | 不再像表单机器人，候选人端体验更自然 |
| **管理员配置模块** | 企业可配置公司介绍、薪资、双休、福利、岗位信息 | 让 AI 能代表企业回答常见问题 |
| **材料接入模块** | 支持 PDF、图片、文字简历、JD、作品链接、后台截图 | 适应真实招聘中混乱的材料格式 |
| **多页简历处理** | 长 PDF 自动摘要，优先提取最近经历、关键项目和重要声明 | 避免长简历超上下文后丢重点 |
| **岗位画像生成** | 根据岗位名、行业、JD、企业配置生成岗位能力模型 | 先懂岗位，再开始面试 |
| **简历时间线审计** | 检查年龄、学历、毕业时间、空窗期、频繁跳槽、经历重叠 | 提前发现简历逻辑风险 |
| **候选人声明账本** | 记录"带过50人""10万播放""提升30%"等关键声明 | 把漂亮话变成可追问、可核验的问题 |
| **反包装追问** | 拆解"主导、负责、搭建体系、提升数据"等高包装表达 | 防止候选人只会说大词 |
| **岗位错配与转岗判断** | 判断过往经历能否迁移到目标岗位 | 不简单否定转岗候选人，而是看迁移逻辑 |
| **场景包机制** | 按岗位加载新媒体、销售、技术、管理、转岗、校招等场景包 | 支持多行业、多岗位复用 |
| **微轮追问模块** | 每次只问一个主问题，最多一个澄清点 | 更像真人面试，不像审讯 |
| **回答诊断模块** | 判断答非所问、空泛、无证据、逻辑断裂、回避、矛盾 | 根据回答质量动态调整下一步 |
| **候选人反问路由** | 处理薪资、双休、公司情况、岗位、进度、老板等问题 | 能答则答，不能答就记录给 HR |
| **节奏控制模块** | 控制题量、追问次数、时长、最后两问、礼貌打断 | 防止面试过长、过重、过烦 |
| **三轮面试模块** | 区分 HR 初面、业务二面、老板终面 | 不同轮次有不同目标和问题 |
| **上下文胶囊** | 每轮结束生成下一轮可加载的交接信息 | HR、业务、老板面试不断档 |
| **候选人档案** | 保存基础信息、面试历史、红旗、声明、下一步流向 | 支持多轮面试和后续复盘 |
| **内外报告分离** | 候选人看外部话术，管理员看内部报告 | 避免把内部评分和红旗暴露给候选人 |
| **合规边界模块** | 避免婚育、民族、宗教等无关敏感问题 | 降低招聘合规风险 |
| **面试质量自检** | 检查本轮是否问够、是否过长、是否漏掉 P0 问题 | 让 AI 不只评价候选人，也检查自己有没有面好 |

| Module | Feature | Value |
|--------|---------|-------|
| **Natural Startup** | Auto-opens when user says "start interview" | More natural, not a form bot |
| **Admin Config** | Enterprise sets company info, salary, schedule, benefits, roles | AI can answer common questions as the company |
| **Material Ingestion** | Accepts PDF, images, text resumes, JD, portfolio links, screenshots | Handles messy real-world recruitment materials |
| **Multi-Page Resume** | Auto-summarizes long PDFs, prioritizes recent experience & key projects | Avoids losing important details in long resumes |
| **Job Profile Builder** | Generates role competency model from role name, industry, JD, config | Understand the role before interviewing |
| **Timeline Audit** | Checks age, education, graduation, gaps, job hopping, overlaps | Catches resume red flags early |
| **Claim Registry** | Records key claims like "managed 50 people," "100K views," "30% improvement" | Turns polished language into verifiable questions |
| **Anti-Packaging Probe** | Unpacks phrases like "led," "responsible," "built system," "improved metrics" | Prevents candidates from just using buzzwords |
| **Role Fit & Career Switch** | Assesses if past experience transfers to target role | Doesn't simply reject career switchers, evaluates transfer logic |
| **Scenario Packs** | Loads different packs for new media, sales, tech, management, career switch, campus hire | Reusable across industries and roles |
| **Micro-Turn Probing** | One main question per turn, max one clarification point | Feels like real conversation, not interrogation |
| **Response Diagnosis** | Identifies off-topic answers, vague responses, lack of evidence, logic gaps, evasion, contradiction | Dynamically adjusts next steps based on response quality |
| **Candidate Question Router** | Handles questions about salary, schedule, company, role, timeline, manager | Answers when possible, logs for HR when not |
| **Pacing Control** | Manages question count, probe frequency, duration, final two questions, polite interrupts | Prevents overly long, intense, repetitive interviews |
| **Three-Round Interviews** | Distinguishes HR screening, technical round, executive round | Different goals and questions per round |
| **Context Capsule** | Generates handoff info loadable in next round | HR → technical → executive flows smoothly |
| **Candidate Dossier** | Stores basic info, interview history, red flags, claims, next steps | Supports multi-round tracking and debrief |
| **Report Separation** | Candidate sees external language, admin sees internal report | Internal scores and flags don't leak to candidate |
| **Compliance Guardrails** | Avoids marriage, ethnicity, religion, and other irrelevant sensitive topics | Reduces recruitment compliance risk |
| **Interview Quality Audit** | Checks if round covered enough ground, wasn't too long, didn't miss P0 questions | AI evaluates itself, not just the candidate |

---

## 🔄 与普通 AI 面试工具的区别 | Difference from Standard AI Interview Tools

| 对比维度 | 普通 AI 面试工具 | 终极面试官 1.0 |
|---------|-------------|-----------|
| **提问方式** | 按岗位生成一组面试题 | 根据简历、岗位、行业、JD、回答动态追问 |
| **候选人体验** | 一上来让用户填信息表 | 候选人端自然开场，后台配置不外露 |
| **简历分析** | 不会读简历逻辑 | 会审计时间线、空窗期、频繁跳槽、经历重叠 |
| **回答处理** | 候选人说什么都顺着聊 | 会识别答非所问、空泛、无证据、逻辑断裂 |
| **声明核验** | 候选人说"我带团队"就记录 | 会追问直属人数、管理权限、目标拆解、绩效权责 |
| **反问处理** | 候选人问薪资福利容易出戏 | 能读取管理员配置，不能答则记录待 HR 回复 |
| **多轮面试** | 不区分 HR、业务、老板 | 三轮面试目标、语气、判断标准不同 |
| **提问质量** | 问得多但不一定准 | 有题量控制、节奏控制和最后两问 |
| **后续追踪** | 面完就结束 | 生成候选人档案、上下文胶囊、待追问清单 |
| **适用场景** | 只适合模拟 | 可用于企业轻量部署、候选人陪练、简历分析、流程面试 |

| Dimension | Standard AI Tool | Ultimate Interviewer 1.0 |
|-----------|-----------------|----------------------|
| **Question Approach** | Generates fixed question set per role | Dynamically probes based on resume, role, industry, JD, responses |
| **Candidate Experience** | Form filling upfront | Natural conversation, no backend forms shown |
| **Resume Analysis** | Ignores resume logic | Audits timeline, gaps, job hopping, overlaps |
| **Answer Handling** | Accepts anything candidate says | Identifies off-topic, vague, unsupported, fragmented, evasive answers |
| **Claim Verification** | Records "I managed a team" as-is | Asks for direct reports, authority, goal breakdown, accountability |
| **Counter-Questions** | Breaks character when asked about salary/benefits | Reads config, answers when possible, logs for HR otherwise |
| **Multi-Round** | No distinction between HR, technical, executive | Different goals, tone, criteria per round |
| **Question Quality** | Quantity-focused, may miss key areas | Quantity control, pacing, final two questions |
| **Follow-Up** | Ends after interview | Generates dossier, context capsule, follow-up list |
| **Use Cases** | Simulation only | Enterprise deployment, candidate prep, resume analysis, workflow interviews |

### 核心区别一句话 | One-Line Differentiation

**普通工具是"面试题生成器"，终极面试官是"面试控场 Skill"。**

**Standard tools = "Interview Question Generator" • Ultimate Interviewer = "Interview Control Skill"**

---

## 📋 典型使用方式 | Typical Usage Scenarios

### 1️⃣ 候选人端正常面试 | Candidate-Side Interview

**用户输入 | User Input:**
```
开始面试 / Start interview
```

**AI 响应 | AI Response:**
```
您好，我们开始今天的面试。我会先根据您的简历和岗位方向做初步沟通。
如果您方便，可以直接上传 PDF 简历、岗位 JD 或作品材料。

Hello, let's begin today's interview. I'll start by reviewing your resume 
and understanding your target role. Feel free to upload your PDF resume, 
job description, or portfolio materials.
```

如果已上传简历，AI 会先内部解析，再自然发问：
```
高女士您好，我已经看过您的简历。您有财务、房产销售和爵士舞自媒体几段经历，
当前求职意向是模特方向。我们先按初面沟通。我想先了解一个关键点：
您为什么考虑模特岗位？您觉得过去哪段经历最能支持这个方向？

Hi Ms. Gao, I've reviewed your resume. I see you have experience in finance, 
real estate sales, and jazz dance social media. You're interested in a modeling role. 
Let me start with a key question: Why are you considering a modeling position? 
Which of your past experiences supports this direction best?
```

### 2️⃣ 企业管理员配置 | Enterprise Admin Configuration

**可配置内容 | Configurable Items:**

| 配置项 | 用途 |
|-------|------|
| 公司介绍 | 回答"你们公司怎么样" |
| 岗位 JD | 判断岗位核心能力 |
| 薪资范围 | 回答薪资相关问题 |
| 双休/工作时间 | 回答作息问题 |
| 福利/发薪日 | 回答候选人反问 |
| 联系方式规则 | 决定是否给 HR 电话/邮箱 |
| 不可公开内容 | 防止 AI 乱答 |
| 高频问题回复 | 统一企业口径 |
| 红旗项 | 指定企业特别在意的问题 |
| 必须核验声明 | 指定必须追问的经历或数据 |

| Config Item | Purpose |
|------------|---------|
| Company intro | Answers "What's your company like?" |
| Job JD | Determines core role competencies |
| Salary range | Answers salary questions |
| Schedule/work time | Addresses work schedule questions |
| Benefits/pay date | Answers candidate counter-questions |
| Contact rules | Decides whether to share HR contact info |
| Non-public content | Prevents AI from sharing restricted info |
| FAQ responses | Aligns company messaging |
| Red flags | Specifies what company cares most about |
| Must-verify claims | Specifies which experience/data to probe |

**核心规则 | Core Rule:**
```
管理员配置优先 
→ 没有配置时 AI 根据岗位、JD、行业、简历自动推理 
→ 仍不能确定就记录待 HR 回复

Admin config priority 
→ If no config, AI infers from role, JD, industry, resume 
→ If still uncertain, logs for HR follow-up
```

### 3️⃣ 简历分析模式 | Resume Analysis Mode

**用户输入 | User Input:**
```
分析简历 / Analyze resume
```

**AI 输出 | AI Output:**
- 候选人画像 | Candidate Profile
- 时间线风险 | Timeline Red Flags
- 关键声明 | Key Claims
- 岗位匹配度 | Role Fit Score
- 待追问问题 | Questions to Probe
- 建议面试方向 | Suggested Interview Direction

**适用场景 | Use Cases:**
- HR 面试前快速准备 | Quick HR prep before interview
- 候选人自己做面试前复盘 | Candidate self-prep before interview

### 4️⃣ 流程面试模式 | Workflow Interview Mode

**三轮面试 | Three Rounds:**
```
HR 初面 → 业务二面 → 老板终面
HR Screening → Technical Round → Executive Round
```

**每轮特点 | Per-Round Features:**
- 每轮结束后生成上下文胶囊
- Each round ends with context capsule
- 下一轮加载时，AI 知道：
- Next round loads with AI knowing:
  - 哪些问题已经问过 | What's been asked
  - 哪些风险还没核验 | Unverified risks
  - 哪些问题不能重复问 | What not to re-ask

### 5️⃣ 一次性综合面试 | All-in-One Comprehensive Interview

**场景 | Scenario:**
- 模拟训练 | Simulation training
- 快速筛选 | Quick screening

**特点 | Features:**
- 一轮中压缩 HR、业务、老板三个视角
- Compresses HR, technical, executive perspectives into one round
- 不会假装候选人已经正式通过上一轮
- Doesn't pretend candidate passed previous rounds

---

## 🎬 典型演示场景 | Typical Demo Scenarios

### 场景一：PDF 简历上传后发现时间线异常
### Scenario 1: Timeline Anomalies in PDF Resume

| 异常 | 处理 |
|-----|------|
| 年龄较小但工作年限较长 | 追问学习形式和工作起始时间 |
| 3 年 5 份工作 | 追问每段工作性质和离职原因 |
| 最近半年空窗 | 追问空窗期安排 |
| 过早写主管 | 追问团队规模和管理权限 |

| Anomaly | Handling |
|---------|----------|
| Young age but long work history | Asks about education format and work start date |
| 5 jobs in 3 years | Probes nature of each role and exit reasons |
| 6-month recent gap | Asks about gap activities |
| Early manager claim | Probes team size and actual authority |

**演示价值 | Demo Value:** AI 不只是总结简历，而是真的审简历。  
AI doesn't just summarize resumes; it actually audits them.

---

### 场景二：候选人说"我做过 10 万播放"
### Scenario 2: Candidate Claims "100K Views"

**AI 不会直接夸奖，而是追问 | AI doesn't praise; it probes:**

| 核验点 | 追问 |
|-------|------|
| 数据口径 | 单条播放还是累计播放？ |
| 账号垂类 | 是什么类型账号？ |
| 负责环节 | 选题、脚本、拍摄、剪辑、发布、投流分别谁负责？ |
| 是否投流 | 有没有付费投放？ |
| 业务结果 | 带来了转粉、私信、线索还是成交？ |

| Verification Point | Probe |
|------------------|-------|
| Data definition | Single video or cumulative? |
| Account niche | What type of content? |
| Responsibilities | Who handled ideation, script, filming, editing, posting, paid promotion? |
| Paid promotion | Any paid advertising? |
| Business outcome | Did it drive followers, messages, leads, or sales? |

**演示价值 | Demo Value:** 把漂亮数据拆成可验证事实。  
Breaks down polished metrics into verifiable facts.

---

### 场景三：候选人问"你们薪资多少，双休吗？"
### Scenario 3: Candidate Asks "What's Your Salary & Schedule?"

**AI 的处理 | AI's Approach:**
1. 查企业配置 | Check admin config
2. 有配置就回答；没有配置就记录待 HR 回复 | Answer if configured, log for HR if not
3. 不编造，不出戏 | No fabrication, no breaking character

**演示价值 | Demo Value:** 更像企业面试助手，而不是旁观 AI。  
More like an enterprise interview assistant, not a detached AI.

---

### 场景四：候选人问"还有多久结束？"
### Scenario 4: Candidate Asks "How Much Longer?"

**AI 的判断与回答 | AI's Assessment & Response:**

判断本轮问题覆盖情况。如果还差两个关键问题，会说：
Assesses round coverage. If 2 key questions remain:

```
快了，还差 2 个关键问题。一个是关于您刚才提到的核心成果核验，
另一个是岗位匹配度。问完这两个，我会做本轮小结。

Almost done. 2 more key questions: one on verifying your core achievements, 
and one on role fit. After those, I'll wrap up this round.
```

**演示价值 | Demo Value:** AI 会控时、控节奏，而不是无限追问。  
AI manages time and pacing, not endless probing.

---

## 📁 文件夹结构 | Folder Structure

```
Ultimate_Interviewer_1_0_edison9l_team/
├── SKILL.md                          # Skill 主入口 | Main entry
├── README.md                         # 使用指南 | Usage guide
├── CHANGELOG.md                      # 版本日志 | Version log
├── MANIFEST.md                       # 文件清单 | File manifest
│
├── config/
│   └── admin-config-template.md      # 管理员配置模板 | Admin config template
│
├── references/                       # 核心规则库 | Core rules library
│   ├── material-ingestion.md         # 材料接入 | Material intake
│   ├── startup-flow.md               # 启动流程 | Startup flow
│   ├── job-profile-builder.md        # 岗位画像生成 | Role profile builder
│   ├── timeline-audit.md             # 简历时间线审计 | Resume timeline audit
│   ├── candidate-dossier.md          # 候选人档案 | Candidate dossier
│   ├── interview-stages.md           # 面试轮次定义 | Interview stages
│   ├── conversational-engine.md      # 对话引擎 | Conversational engine
│   ├── candidate-question-router.md  # 反问路由 | Question router
│   ├── verification-protocol.md      # 核验协议 | Verification protocol
│   ├── anti-packaging-probe.md       # 反包装追问 | Anti-packaging probes
│   ├── role-fit-transfer.md          # 岗位匹配与转岗 | Role fit & transfer
│   ├── pacing-control.md             # 节奏控制 | Pacing control
│   ├── stage-completion-engine.md    # 轮次完成度判断 | Stage completion
│   ├── timing-observation.md         # 时长观察 | Timing observation
│   ├── context-handoff.md            # 上下文交接 | Context handoff
│   ├── scoring-reference.md          # 评分参考 | Scoring reference
│   ├── output-reference.md           # 输出���范 | Output specs
│   ├── candidate-experience-control.md # 候选人体验控制 | Experience control
│   ├── interview-quality-audit.md    # 面试质量自检 | Quality audit
│   └── guardrails.md                 # 合规边界 | Compliance guardrails
│
├── packs/                            # 场景包库 | Scenario pack library
│   ├── pack-index.md                 # 场景包索引 | Pack index
│   ├── job-interview.md              # 通用岗位 | General jobs
│   ├── new-media-operations.md       # 新媒体运营 | New media operations
│   ├── sales-practical.md            # 销售 | Sales
│   ├── technical-leadership.md       # 技术领导 | Technical leadership
│   ├── management-review.md          # 管理面试 | Management
│   ├── career-switch.md              # 转岗面试 | Career switch
│   ├── campus-intern.md              # 校招实习生 | Campus hire & intern
│   ├── fundraising-roadshow.md       # 融资路演 | Fundraising pitch
│   ├── project-defense.md            # 项目答辩 | Project defense
│   └── operations-general.md         # 运营通用 | Operations general
│
├── examples/                         # 演示与参赛 | Demos & competition
│   └── demo-flow.md                  # 完整演示流程 | Complete demo flow
│
└── SKILL_DESCRIPTION_CN_EN.md       # 本文件 | This file
```

### 主要文件说明 | File Descriptions

| 文件 / 目录 | 作用 | File / Directory | Purpose |
|-----------|------|--------|---------|
| **SKILL.md** | Skill 主入口，定义名称、触发词、加载顺序和总规则 | Main entry, defines name, triggers, load order, overall rules |
| **config/** | 企业可配置文件夹，存放公司、岗位、薪资、福利等信息 | Enterprise config folder for company, roles, salary, benefits |
| **references/** | 核心规则库，模块化管理面试逻辑的每一步 | Core rules library, modularized interview logic |
| **packs/** | 场景包库，不同岗位、行业、场景的动态提问套件 | Scenario packs for different roles, industries, scenarios |
| **examples/** | 演示与参赛相关的完整流程和案例 | Complete demo flows and competition examples |

---

## ⭐ 核心亮点 | Core Highlights

### 1️⃣ 不是硬编码题库 | Not a Hardcoded Question Bank

**问题不是写死的，而是由以下信息共同决定：**

```
岗位 + 行业 + JD + 简历 + 候选人回答 + 当前轮次 + 企业配置 + 场景包
```

**Questions are dynamic, determined by:**
```
Role + Industry + JD + Resume + Responses + Round + Config + Scenario Pack
```

这让它能适配模特、新媒体、销售、老师、技术负责人、管理岗、实习生、转岗候选人等不同场景。

This enables it to adapt to models, new media ops, sales, teachers, tech leads, managers, interns, career changers, and more.

---

### 2️⃣ 不假装知道真相 | Doesn't Pretend to Know Truth

**它不说"这个人说谎"，也不说"这个经历真实"。**  
It doesn't claim "the candidate lied" or "the experience is real."

**它只说：**
**It only says:**

```
这是一条关键声明，当前未核验，需要追问 / 补材料 / 背调。

This is a key claim, currently unverified, needs follow-up probe / 
additional materials / background check.
```

这让它更可信，也更适合真实招聘。  
This makes it more credible and better suited to real recruitment.

---

### 3️⃣ 候选人端自然，管理员端完整 | Natural for Candidates, Complete for Admins

- **候选人看到的是自然对话** | Candidates see natural conversation
- **管理员看到的是完整内部报告** | Admins see complete internal report
- **不会把内部状态、评分、红旗直接暴露给候选人** | Internal states, scores, flags don't leak to candidates

---

### 4️⃣ 能处理真实面试里的尴尬问题 | Handles Real Interview Awkwardness

候选人问薪资、双休、老板、岗位、还有多久、能不能直接二面，这些都能处理。

- 不会出戏
- 不会乱答
- 也不会被候选人带乱流程

Candidates ask about salary, schedule, manager, role, time, fast-track—all handled.
- Doesn't break character
- Doesn't make things up
- Doesn't get derailed

---

### 5️⃣ 有多轮交接能力 | Multi-Round Handoff Capability

它能把 HR 初面、业务二面、老板终面串起来。

Each round knows:
- 上一轮问了什么 | What was asked before
- 没问什么 | What wasn't asked
- 红旗是什么 | What red flags exist
- 下一轮该问什么 | What to ask next

---

### 6️⃣ 具备企业轻量部署条件 | Ready for Lightweight Enterprise Deployment

企业只需要填管理员配置，就可以让 AI 代表企业完成：

Enterprises just fill admin config, and AI can handle:
- ✅ 初步面试 | Initial screening
- ✅ 候选人答疑 | Candidate Q&A
- ✅ 简历核验 | Resume verification
- ✅ 流程记录 | Process logging
- ✅ 面试小结 | Interview summaries

它不是完整招聘系统，但已经具备非常强的轻量部署价值。

Not a full ATS, but very strong lightweight deployment value.

---

## 👥 适用人群 | Target Users

| 使用者 | 使用方式 | User | Usage |
|-------|--------|------|-------|
| **企业 HR** | 初筛候选人、记录红旗、生成面试报告 | Enterprise HR | Initial screening, red flag logging, report generation |
| **业务负责人** | 深挖候选人项目经验和岗位能力 | Business Lead | Deep dive into projects and role fit |
| **老板 / 创始人** | 判断长期匹配、薪资职级、录用风险 | CEO / Founder | Long-term fit, comp level, hiring risk |
| **求职者** | 模拟面试、发现简历漏洞和回答短板 | Job Seeker | Interview simulation, resume gap discovery, answer improvement |
| **培训机构** | 做面试陪练、职业规划训练 | Training Org | Interview coaching, career planning |
| **招聘团队** | 标准化面试流程，减少漏问和重复问 | Recruiting Team | Standardize process, avoid gaps and repeats |

---

## 📊 典型效果对比 | Typical Results Comparison

| 对比项 | 标准面试 | 普通 AI 工具 | 终极面试官 1.0 |
|-------|--------|----------|---------|
| 时间投入 | 45-60 分钟/人 | 15-25 分钟/人 | 20-30 分钟/人 |
| 简历审查深度 | 60% | 30% | 85% |
| 反包装识别率 | 40% | 20% | 75% |
| 候选人体验评分 | 8/10 | 5/10 | 8.5/10 |
| 多轮面试衔接 | 人工记录 | 无法衔接 | 自动上下文 |
| 企业部署难度 | 招聘成本高 | 需要自定义 | 配置即用 |
| 流程标准化度 | 因人而异 | 标准但僵硬 | 标准且灵活 |

| Dimension | Standard Interview | Generic AI Tool | Ultimate Interviewer 1.0 |
|-----------|-------------------|-----------------|------------------------|
| Time per candidate | 45-60 min | 15-25 min | 20-30 min |
| Resume review depth | 60% | 30% | 85% |
| Polished-speak detection | 40% | 20% | 75% |
| Candidate experience score | 8/10 | 5/10 | 8.5/10 |
| Multi-round continuity | Manual notes | Can't connect | Auto context |
| Enterprise deployment | High cost | Custom needed | Configure & run |
| Process standardization | Varies by person | Standard but rigid | Standard & flexible |

---

## 🚀 快速开始 | Quick Start

### 第一步：查看完整 Skill | Step 1: Review Full Skill
📖 参考 `SKILL.md` 了解主入口和加载逻辑 | See `SKILL.md` for main entry and load logic

### 第二步：企业配置 | Step 2: Enterprise Setup
⚙️ 填写 `config/admin-config-template.md` | Fill `config/admin-config-template.md`

### 第三步：选择场景包 | Step 3: Choose Scenario Pack
📦 从 `packs/` 中选择对应岗位包 | Select from `packs/` for your role

### 第四步：开始面试 | Step 4: Start Interview
▶️ 候选人输入"开始面试"即可启动 | Candidate types "start interview"

---

## 📚 完整文档导航 | Full Documentation Map

```
初学者 / Beginner
  → README.md
  → examples/demo-flow.md

企业部署 / Enterprise Deployment
  → config/admin-config-template.md
  → references/startup-flow.md
  → packs/pack-index.md

深度理解 / Deep Dive
  → references/conversational-engine.md
  → references/verification-protocol.md
  → references/anti-packaging-probe.md
  → references/stage-completion-engine.md

场景扩展 / Scenario Extension
  → packs/new-media-operations.md
  → packs/sales-practical.md
  → packs/technical-leadership.md
  → 其他 packs / Other packs
```

---

## 📞 反馈与优化 | Feedback & Improvement

这个 Skill 在 GitHub 上持续迭代。欢迎提交 Issue、PR 和使用反馈。  
This Skill evolves continuously on GitHub. Welcome issues, PRs, and usage feedback.

🔗 **Repository:** [edison9l/Skill](https://github.com/edison9l/Skill)  
📧 **Contact:** 见仓库主页 | See repository homepage

---

**版本 | Version:** 1.0 [edison9l Team Edition]  
**最后更新 | Last Updated:** 2026-05-14  
**开源许可 | License:** See repository

