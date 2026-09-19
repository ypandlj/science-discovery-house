<p align="center">
  <img src="public/logo-horizontal.png" alt="科学探索屋" width="420"/>
</p>

<p align="center">
  <strong>科学探索屋</strong> · Science Discovery House
</p>

<p align="center">
  面向小学科学的 AI 互动探究课堂 —— 说一句需求，学生自己“探”出科学
</p>

<p align="center">
  <img src="https://img.shields.io/badge/License-MIT-green.svg?style=flat-square" alt="License: MIT"/>
  <img src="https://img.shields.io/badge/Next.js-16-black?style=flat-square&logo=next.js" alt="Next.js"/>
  <img src="https://img.shields.io/badge/React-19-61DAFB?style=flat-square&logo=react&logoColor=white" alt="React"/>
  <img src="https://img.shields.io/badge/TypeScript-5-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript"/>
  <img src="https://img.shields.io/badge/LangGraph-1.1-purple?style=flat-square" alt="LangGraph"/>
  <img src="https://img.shields.io/badge/Tailwind_CSS-4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS"/>
</p>

<p align="center">
  <a href="#1-项目简介">项目简介</a> ·
  <a href="#2-内置课程物体的运动8-课">内置课程</a> ·
  <a href="#3-核心能力">核心能力</a> ·
  <a href="#4-快速开始">快速开始</a> ·
  <a href="#5-模型与语音服务商">服务商配置</a> ·
  <a href="#6-部署">部署</a> ·
  <a href="#7-二次开发说明">二次开发</a> ·
  <a href="#8-常见问题">常见问题</a>
</p>

---

## 1. 项目简介

**科学探索屋**（Science Discovery House）是一个面向**小学科学**学科的 AI 互动探究课堂。它把“一节课”变成一段可以点、可以看、可以动手、可以提问的探究过程：AI 老师负责讲解，AI 同学负责追问和讨论，学生则负责在虚拟实验里调参数、做预测、看结果。

本产品定位为**学生自学与自主探究工具**：不需要教师现场操作，学生打开网页、点选一个课时，几分钟内就能得到一整堂可播放、可交互的科学课；教师也可以用它快速生成课件与课堂素材。

它解决的问题很具体——科学课最需要“动手”，但器材、场地、课时都很有限；而常见的 AI 生成内容又只是“换了一种形式的看视频”。科学探索屋把**虚拟实验**和**迷思概念挑战**写进了生成规则，让每一课都必须包含“能被操作、能被验证”的环节。

> **技术底座说明：** 本项目基于清华大学 THU-MAIC 团队的开源项目 **OpenMAIC**（Open Multi-Agent Interactive Classroom）二次开发，遵循 MIT 协议，保留原项目许可证与致谢。产品化的品牌、课程内容、提示词与学科知识库均在本仓库中完成。

<!-- 演示视频 / 动图占位：上传后可在此插入，例如
<p align="center"><img src="docs/demo.gif" width="720"/></p>
-->

### 核心亮点

- **一句话生成整堂课** —— 描述课题，或直接点选内置课时，AI 自动完成大纲与全部场景
- **多智能体课堂** —— AI 老师与不同人设的 AI 同学实时讲解、讨论、互相提问
- **可动手的虚拟实验** —— 学生调节参数、观察现象、验证预测，而不是被动看视频
- **迷思概念先破后立** —— 先抛出学生的常见错误直觉，再让学生预测、用实验揭示真相
- **白板 + 语音讲解** —— 智能体在共享白板上实时画图、写公式，并把过程讲出来
- **一键导出** —— 导出可编辑的 `.pptx` 课件，或可离线播放的交互式 `.html`
- **模型中立** —— 大模型、语音、图像/视频、联网搜索均可自由替换，不绑定单一厂商

---

## 2. 内置课程：《物体的运动》8 课

内置**教科版小学科学三年级上册第三单元《物体的运动》**全部 8 课。首页对话框下方即为一排课时快捷按钮，**点一下就直接开始生成这一课**（若尚未配置任何模型，会自动打开设置面板引导配置）。

| 课次 | 课题 | 核心概念 | 要正面挑战的迷思概念 |
|---|---|---|---|
| 1 | 运动和位置 | 判断运动/静止必须先选定参照物；用相对于参照物的位置变化描述运动 | “不动的物体就是静止的”——忽略参照物 |
| 2 | 各种各样的运动 | 运动形式多样：平移、转动、摆动、振动、滚动 | “只有位置移动才算运动” |
| 3 | 直线运动和曲线运动 | 运动路线分为直线运动与曲线运动 | “拐弯的轨迹没有规律、不必描述” |
| 4 | 物体在斜面上运动 | 运动方式（滑动/滚动）与物体形状有关；斜面越陡，运动越快 | “物体越重，下滑越快”（实际与质量无关） |
| 5 | 比较相同距离内运动的快慢 | 距离相同时，用时短的更快 | “跑在前面的一定更快”（忽略距离是否相同） |
| 6 | 比较相同时间内运动的快慢 | 时间相同时，路程长的更快 | 混淆“比时间”与“比距离”两种比较口径 |
| 7 | 我们的“过山车” | 设计并搭建轨道，让小球按指定路线运动；坡度与弯道影响运动 | “只要有坡度小球就会一直加速” |
| 8 | 测试“过山车” | 用测试数据比较、发现问题并改进 | “一次成功就说明轨道稳定可靠” |

**每一课都必须满足的生成要求**（写进了学科知识库，AI 生成时会被强制注入）：

- 必须包含**可交互的虚拟实验**（如斜面小车、轨道小车），学生可以调参并观察现象；
- 必须显式**先呈现迷思概念 → 引导学生预测 → 用实验揭示真相**（反直觉 → 预测 → 验证）；
- 面向小学三年级，语言浅显，多用生活实例（滑梯、过山车、跑步比赛）；
- 不使用超纲概念（避免加速度、牛顿运动定律、重力加速度公式等）。

> **想换成自己的单元？** 只需替换学科知识库文件和首页课时清单两处，代码框架无需改动，详见[第 7 节：二次开发说明](#7-二次开发说明)。

---

## 3. 核心能力

### 3.1 多智能体互动课堂

课堂不是“播放一段视频”，而是由多个智能体共同推进：

- **课堂讨论** —— 智能体主动发起话题，学生可以随时插话或“被点名”
- **圆桌辩论** —— 多个不同人设的智能体围绕一个科学问题各说各的理，配合白板讲清依据
- **自由问答** —— 学生随时提问，AI 老师用幻灯片、示意图或白板现场解答
- **白板讲解** —— 智能体在共享白板上实时作图：画斜面、标方向、写数据

编排层基于 **LangGraph** 状态机驱动机器人轮次（说话、画图、点聚焦、放激光笔），播放层则是一套状态机（idle → playing → live），因此“课堂回放”和“实时对话”共用同一套场景数据。

### 3.2 探究式生成：两阶段流水线

| 阶段 | 做什么 |
|---|---|
| **大纲生成** | 分析学生的需求与上传材料，产出结构化的课堂大纲（含每课的核心概念与探究环节） |
| **场景生成** | 把每个大纲条目变成可播放的场景——幻灯片、测验、交互式虚拟实验、项目式学习（PBL） |

生成时会把学科知识库（见第 7 节）作为提示词片段注入，因此产出的内容会遵守“先迷思、后验证、必含虚拟实验”的规则。

### 3.3 深度交互模式：五种交互界面

**被动听讲？不。动手探索才是。**

| 类型 | 用途 |
|---|---|
| **3D 可视化** | 用三维呈现抽象结构，让“看不见的运动”变得直观 |
| **模拟实验** | 流程与实验环境模拟，学生调参后观察动态变化和结果 |
| **游戏** | 知识小游戏，通过交互挑战加深理解与记忆 |
| **思维导图** | 结构化知识组织，帮助学生建立整体概念框架 |
| **在线编程** | 浏览器内编码与即时运行，边写边学边改 |

生成的交互界面全部**响应式**，桌面、平板、手机均可使用；AI 老师还可以主动操作界面来引导注意——高亮关键区域、设置条件、在恰当时机给出提示。

### 3.4 课堂组件

| 组件 | 说明 |
|---|---|
| **幻灯片** | AI 老师配合语音讲解、聚光灯与激光笔动作，接近真实课堂 |
| **测验** | 单选 / 多选 / 简答，支持 AI 实时判分与反馈 |
| **交互式模拟** | 基于 HTML 的交互实验：物理模拟器、流程图等 |
| **项目式学习（PBL）** | 选择角色，与 AI 智能体协作完成有里程碑和交付物的项目 |

### 3.5 导出与离线使用

| 格式 | 说明 |
|---|---|
| **PowerPoint（.pptx）** | 可编辑的幻灯片，含图片、图表与 LaTeX 公式 |
| **交互式 HTML** | 自包含网页，含交互式模拟实验，可单独分发 |
| **课堂 ZIP** | 完整课堂导出（课程结构 + 媒体文件），用于备份、分享与迁移 |

**离线 / 内网播放：** 导出课堂或资源包时，会把交互场景引用的外部资源（KaTeX、Three.js、Tailwind CDN、字体、图片）以 `data:` URI 形式内联进 HTML。导出的课程导入到内网或离线实例后即可完全离线播放，播放时不再访问任何公网 CDN；导出时抓取失败的外部资源会被记录并保留原始 URL。

### 3.6 教学与体验

- **语音合成（TTS）** —— 多种语音服务商，支持自定义音色，为讲解自动生成旁白
- **语音识别（ASR）** —— 学生可以用麦克风和 AI 老师对话
- **联网搜索** —— 智能体在课堂中检索最新信息
- **课件编辑器** —— 生成的幻灯片可直接在浏览器内编辑（拖拽、缩放、旋转、多选），也可用“AI 编辑”按指令改
- **多语言界面** —— 简体中文、繁体中文、英文、日文、韩文、俄文、阿拉伯文、葡萄牙文（巴西）、西班牙文（墨西哥）、法文、越南文、德文
- **暗色模式** —— 夜间使用更护眼

---

## 4. 快速开始

### 4.1 环境要求

- **Node.js** >= 22.19（仓库 `.nvmrc` 指定为 22）
- **pnpm** >= 10

### 4.2 获取代码并安装依赖

```bash
git clone https://github.com/ypandlj/science-discovery-house.git
cd science-discovery-house
pnpm install
```

> `postinstall` 会自动构建工作区子包（`@openmaic/*`、`pptxgenjs`、`mathml2omml`），首次安装需要几分钟。

### 4.3 配置模型

```bash
cp .env.example .env.local
```

`.env.local` 中**至少填写一个大模型服务商的 API Key** 即可启动：

```env
OPENAI_API_KEY=sk-...
ANTHROPIC_API_KEY=sk-ant-...
GOOGLE_API_KEY=...
DEEPSEEK_API_KEY=...
DASHSCOPE_API_KEY=...
```

也可以不碰配置文件，直接在页面右上角的**设置 → 模型服务商**里填写（配置保存在浏览器本地，见第 8 节说明）。

### 4.4 启动

```bash
pnpm dev
```

打开 **http://localhost:3000** ，在首页点选一个课时按钮，或直接输入一句话需求。

### 4.5 生产环境构建

```bash
pnpm build && pnpm start
```

### 4.6 可选：站点访问密码（ACCESS_CODE）

对外分享或部署到公网时，建议加一道站点级口令：

```env
ACCESS_CODE=your-secret-code
```

设置后，访问者需要先输入口令才能进入，所有 API 路由同样受保护；不设置则和原来一样。口令会以签名令牌存在 HTTP-only Cookie 中、有效期 7 天。请使用至少 16 位的随机值——它是保护部署的唯一密钥。

### 4.7 常用命令

| 命令 | 作用 |
|---|---|
| `pnpm dev` | 启动开发服务器（http://localhost:3000） |
| `pnpm build` | 生产构建 |
| `pnpm start` | 运行生产构建产物 |
| `pnpm test` | 运行单元测试（Vitest） |
| `pnpm lint` | ESLint 检查 |
| `pnpm check` / `pnpm format` | Prettier 检查 / 格式化 |

---

## 5. 模型与语音服务商

### 5.1 支持的模型服务商

**OpenAI**、**Azure OpenAI**、**Anthropic**、**Amazon Bedrock**、**Google Gemini**、**DeepSeek**、**通义千问 Qwen**、**Kimi**、**MiniMax**、**Grok (xAI)**、**OpenRouter**、**TokenDance**、**豆包（火山方舟）**、**腾讯混元 / TokenHub**、**小米 MiMo**、**智谱 GLM**、**Ollama**（本地）、**Lemonade**（本地 LLM/图像/TTS/ASR）、**FunASR**（本地语音识别），以及任何兼容 OpenAI API 的服务。

### 5.2 推荐配置

> **推荐：** 把全部模态都打开时效果最好——自动配图、语音旁白、视频片段、联网检索都会参与生成。最省事的做法是用**一个 Key 覆盖全部模态**（例如 TokenDance 这类聚合网关），默认模型选择 `deepseek-v4.1-flash` 之类速度快、上下文长的模型。

常用服务商示例：

```env
# OpenAI
OPENAI_API_KEY=sk-...
DEFAULT_MODEL=openai:gpt-5.5

# 智谱 GLM（国内站）
GLM_API_KEY=...
GLM_BASE_URL=https://open.bigmodel.cn/api/paas/v4
DEFAULT_MODEL=glm:glm-5.1

# MiniMax
MINIMAX_API_KEY=...
MINIMAX_BASE_URL=https://api.minimaxi.com/anthropic/v1
DEFAULT_MODEL=minimax:MiniMax-M2.7-highspeed

# 小米 MiMo Token Plan
MIMO_API_KEY=tp-...
MIMO_BASE_URL=https://token-plan-cn.xiaomimimo.com/v1
DEFAULT_MODEL=xiaomi:mimo-v2.5-pro

# Amazon Bedrock
BEDROCK_REGION=us-east-1
BEDROCK_MODELS=us.anthropic.claude-sonnet-5
DEFAULT_MODEL=bedrock:us.anthropic.claude-sonnet-5
```

### 5.3 语音合成（TTS）配置要点

课程旁白依赖 TTS。国内网络环境下，**豆包 TTS 2.0（火山引擎）** 是实测最稳的选择，填写方式如下：

- **App ID**：火山控制台中的 `APP ID`
- **Access Key / API Key**：火山控制台中的 `Access Token`（`Secret Key` 用不到）
- **Base URL**：`https://openspeech.bytedance.com/api/v3/tts`

```
注意：域名是 openspeech.bytedance.com（.com），且 Base URL 不需要带 /unidirectional，
程序会自动补全；如果页面上显示 .co 结尾，说明填错了。
```

程序按填写的 Key 形态自动选择认证方式：若是 `AppID:AccessToken` 形式，走 `X-Api-App-Id` + `X-Api-Access-Key` 调用 `/api/v3/tts/unidirectional`；若只填单个 Key，则走 `/api/plan/tts` + `X-Api-Key`（Agent Plan 模式）。

也可以使用本地方案：**VoxCPM2**（自托管 TTS，支持音色克隆）、**Lemonade**、**FunASR**（语音识别）：

```env
TTS_VOXCPM_BASE_URL=http://localhost:8000/v1
LEMONADE_BASE_URL=http://localhost:13305/v1
ASR_FUNASR_BASE_URL=http://localhost:8000/v1
```

### 5.4 配置存在哪里（很重要）

默认情况下，页面上填写的 Key **保存在浏览器本地**（按域名隔离）。这意味着：

- 换一台电脑、换一个浏览器，配置就是空的，需要重新填写；
- 服务器重新部署（域名或端口不变）通常不影响本地配置；
- 如果希望“学生打开网页即可用、无需配置”，需要启用**服务端托管配置**（`server-providers.yml` 或环境变量），Key 只保存在服务器、不下发浏览器——详见[第 6.4 节](#64-进阶可选服务器托管配置多人免配置)。

---

## 6. 部署

### 6.1 方式一：Vercel（最省事）

1. Fork 或导入本仓库到 [Vercel](https://vercel.com/new)
2. 配置环境变量（至少一个模型 API Key）
3. 部署

### 6.2 方式二：Docker

```bash
cp .env.example .env.local
# 编辑 .env.local 填入 API Key，然后：
docker compose up --build
```

国内网络构建加速（可选，仅使用公共镜像地址，不要在其中放账号或令牌）：

```bash
ALPINE_MIRROR=mirrors.tuna.tsinghua.edu.cn \
NPM_REGISTRY=https://registry.npmmirror.com \
docker compose up --build
```

### 6.3 方式三：自有服务器（Ubuntu + pnpm + pm2）

适用于云服务器（如腾讯云轻量应用服务器）：

```bash
# 1) 上传源码（或用 git clone），进入目录
cd /home/ubuntu/science-discovery-house

# 2) 安装依赖并构建
pnpm install
pnpm build

# 3) 用 pm2 常驻运行
pm2 start pnpm --name science-house -- start
pm2 save
```

**小内存服务器注意事项（2 核 2G 实测）：**

- `next build` 的类型检查阶段容易内存不足（OOM）。建议先加 **swap**（例如 8G）并放宽 Node 堆内存：
  ```bash
  sudo fallocate -l 8G /swapfile && sudo chmod 600 /swapfile && sudo mkswap /swapfile && sudo swapon /swapfile
  export NODE_OPTIONS=--max-old-space-size=6144
  ```
- 内存极小时，也可在构建期跳过类型检查（仅影响构建期校验，不影响运行）；建议本地开发时保留类型检查。
- **端口放行**：除系统防火墙外，云厂商控制台的“防火墙/安全组”也要放行对应端口（默认 `3000`），否则外网访问不通。

### 6.4 进阶可选：服务器托管配置（多人免配置）

若希望学生端“打开即用”，把服务商配置放到服务器而不下发到浏览器。程序会读取项目根目录的 `server-providers.yml`（或对应环境变量），前端会自动合并并选中，用户无需填写任何 Key。注意：该文件属于服务器机密配置，重新部署时需从安全位置恢复，不要把 Key 提交进仓库。

### 6.5 进阶可选：服务端持久化（PostgreSQL）

默认情况下，课程数据保存在浏览器本地；启用服务端持久化后，课程文档、会话与资源改由服务端存储，多台设备可以共享同一份课件：

```bash
cp .env.example .env.local
printf '\nDATABASE_URL=postgres://openmaic:openmaic-dev@postgres:5432/openmaic\nPERSISTENCE_DEV_TOKEN=openmaic-local-dev\n' >> .env.local
NEXT_PUBLIC_PERSISTENCE=1 NEXT_PUBLIC_PERSISTENCE_TOKEN=openmaic-local-dev docker compose --profile server-persistence up --build
```

> `NEXT_PUBLIC_PERSISTENCE` 是**编译期开关**，会打进浏览器 bundle，构建时与运行时的 token 必须一致。该模式默认的 token 不具备真正的保密性，**仅适用于本地或可信网络内的单用户部署**；正式对外使用前，请替换 `lib/persistence/server-auth.ts` 为真实会话校验。

### 6.6 可选：MP4 视频导出

“导出视频”菜单在浏览器内构建一个自包含的 Hyperframes 项目，转成 MP4 需要 Chromium + FFmpeg，因此由独立的 `render-service` 容器承担：

```bash
docker compose --profile video-export up --build
```

应用会通过 `RENDER_SERVICE_URL` 自动探测该服务并启一键 MP4 渲染；未启用时，导出会退化为下载工程 ZIP，由本地 CLI 渲染。

---

## 7. 二次开发说明

本节说明本项目相对上游 OpenMAIC **具体做了什么**，以及**如何改成你自己的学科**。

### 7.1 界面与品牌

| 位置 | 作用 |
|---|---|
| `lib/brand/brand-config.ts` | 产品名、短名、Logo、站标（favicon）、主题色，是品牌的唯一来源 |
| `app/layout.tsx` | 页面标题与站点元信息 |
| `app/page.tsx` | 首页标题与页脚文案 |
| `public/logo-horizontal.png`、`public/openmaic-mark.png` | 横向 Logo 与方形站标资源 |

### 7.2 首页课时速选

`app/page.tsx` 中的 `SCIENCE_UNIT_TOPICS` 定义了 8 个课时按钮，`buildUnitRequirement()` 负责把按钮转成生成需求：

```
请为小学三年级学生生成科学课《物体的运动》中的一课：“<课题>”，
要求包含多智能体的互动讲解，以及学生可以动手操作的虚拟实验。
```

点击按钮后会立即开始生成；若尚未配置模型，则自动打开设置面板引导配置。

### 7.3 学科知识库（本项目的核心二次开发）

| 文件 | 作用 |
|---|---|
| `lib/prompts/snippets/science-g3-u3.md` | 单元知识库：单元总目标、8 课的核心概念与迷思概念、生成要求 |
| `lib/prompts/templates/interactive-outlines/user.md` | 通过 `{{snippet:science-g3-u3}}` 把知识库注入探究式生成模板 |
| `lib/prompts/types.ts` | 声明该片段 id，供提示词加载器解析 |

生成时，知识库会作为提示词片段一起送给模型，从而保证：内容围绕本单元、每课含虚拟实验、先挑战迷思概念、语言不超纲。

### 7.4 语音旁白默认开关

`lib/store/settings.ts` 中做了联动：当用户配置了一个**可用的云端 TTS**（非浏览器内置朗读）时，会自动打开 `ttsEnabled` 总开关。这样可避免“课生成好了却没有声音”这一常见困惑。

### 7.5 如何替换成你自己的学科

1. 复制一份 `lib/prompts/snippets/science-g3-u3.md`，改成你的年级与单元（课时清单 + 核心概念 + 迷思概念 + 生成要求）；
2. 在 `lib/prompts/types.ts` 中登记新的片段 id，并在模板里用 `{{snippet:<你的片段id>}}` 注入；
3. 修改 `app/page.tsx` 的 `SCIENCE_UNIT_TOPICS`，换成你的课时按钮；
4. 需要换品牌时改 `lib/brand/brand-config.ts` 与 `public/` 下的图片资源。

### 7.6 不建议改动的部分

- 工作区包名与导入路径 `@openmaic/*`（改名会破坏构建与包依赖）
- 环境变量前缀（`OPENMAIC_*` 等）与 `docker-compose.yml` 中的服务名、数据库名
- 运行时全局变量、HTTP 头、SSE 事件标记等内部协议标识
- 导出/导入相关的固定标识（课堂 ZIP 的 MIME 类型、导出目录名等）

> 二次开发遵循一个原则：**只改“内容与外观”，不动“协议与依赖”**，这样升级上游或迁移部署都不会踩坑。

---

## 8. 常见问题

**Q：页面能打开，但点课时按钮后打开了设置面板？**
说明还没有配置可用的模型。请先在设置里填写至少一个模型服务商的 API Key，或配置 `.env.local`。

**Q：换个浏览器 / 换台电脑，之前填的 Key 就没了？**
默认配置保存在浏览器本地（按域名隔离），属预期行为。多人共用或学生自学的场景，建议启用[服务器托管配置](#64-进阶可选服务器托管配置多人免配置)。

**Q：单个语音“测试”按钮能播放，但生成整堂课时报“语音合成失败”？**
通常是 TTS 服务商的并发或长文本限制导致。实测可切换到**豆包 TTS 2.0**（配置方法见[第 5.3 节](#53-语音合成tts配置要点)），并确认 Base URL 为 `https://openspeech.bytedance.com/api/v3/tts`。

**Q：生成的课程没有声音？**
确认已配置云端 TTS 且“语音合成”总开关为开；程序会在检测到可用云端 TTS 后自动打开该开关，若曾手动关闭需重新打开。

**Q：2 核 2G 服务器上 `pnpm build` 中途失败 / 进程被杀？**
内存不足。按[第 6.3 节](#63-方式三自有服务器ubuntu--pnpm--pm2)加 swap 并设置 `NODE_OPTIONS=--max-old-space-size=6144`。

**Q：服务器里跑起来了，但外网访问不了？**
除系统防火墙外，还要在云厂商控制台的“防火墙 / 安全组”放行对应端口（默认 `3000`）。

**Q：课后想给学生发课件？**
用“导出”功能：`.pptx` 便于二次编辑，交互式 `.html` 可直接播放（含离线支持），课堂 ZIP 用于完整备份与迁移。

**Q：国内网络安装依赖或构建很慢？**
Docker 构建可用 `ALPINE_MIRROR` 与 `NPM_REGISTRY` 指定公共镜像源；本地安装可配置 pnpm 使用 `registry.npmmirror.com`。

**Q：想让界面显示为英文？**
界面支持 12 种语言设置，但本产品的课程内容与知识库为中文（面向国内小学科学课堂）。如需英文内容，可替换学科知识库片段并调整生成模板。

---

## 9. 项目结构

```
science-discovery-house/
├── app/                        # Next.js App Router
│   ├── api/                    #   生成、媒体、持久化与智能体 API
│   │   ├── agent/              #     会话、事件、素材与技能控制面
│   │   ├── stages/             #     课程读写、清单与场景获取
│   │   ├── generate/           #     场景生成流水线（大纲、内容、图片、TTS…）
│   │   ├── generate-classroom/ #     异步课堂生成提交与轮询
│   │   ├── chat/               #     多智能体讨论（SSE 流式）
│   │   ├── pbl/                #     项目式学习端点
│   │   ├── persistence/        #     内嵌持久化服务
│   │   ├── export-video/       #     MP4 视频导出
│   │   └── ...                 #     quiz-grade、parse-pdf、web-search、transcription 等
│   ├── classroom/[id]/         #   课堂播放页
│   └── page.tsx                #   首页（课时速选 + 生成输入）
│
├── lib/                        # 核心业务逻辑
│   ├── prompts/                #   提示词模板与学科知识库片段 ← 课程内容定制在这里
│   │   ├── snippets/           #     science-g3-u3.md（本单元知识库）
│   │   └── templates/          #     生成与智能体系统提示词模板
│   ├── brand/                  #   品牌配置 ← 产品名与 Logo 在这里
│   ├── generation/             #   两阶段课堂生成流水线
│   ├── orchestration/          #   LangGraph 多智能体编排（导演图）
│   ├── playback/               #   回放状态机（idle → playing → live）
│   ├── action/                 #   动作执行引擎（语音、白板、特效）
│   ├── ai/                     #   大模型服务商抽象层
│   ├── audio/                  #   TTS 与 ASR 服务商
│   ├── media/                  #   图片与视频生成服务商
│   ├── export/                 #   PPTX 与 HTML 导出
│   ├── store/                  #   Zustand 状态管理（含 TTS 总开关联动）
│   ├── i18n/                   #   国际化
│   └── ...                     #   persistence、server、pdf、web-search、utils 等
│
├── components/                 # React UI 组件
│   ├── slide-renderer/         #   基于 Canvas 的幻灯片编辑与渲染
│   ├── scene-renderers/        #   测验、交互、PBL 场景渲染器
│   ├── chat/                   #   对话区与会话管理
│   ├── settings/               #   设置面板（服务商、TTS、ASR、媒体…）
│   ├── whiteboard/             #   基于 SVG 的白板绘图
│   └── ...                     #   agent、audio、roundtable、stage、ui
│
├── packages/                   # 工作区子包（框架能力，一般不改）
│   ├── @openmaic/dsl/          #   课程/幻灯片数据契约与校验
│   ├── @openmaic/generation/   #   生成契约、流水线与提示词资产
│   ├── @openmaic/renderer/     #   幻灯片 DSL 渲染
│   ├── @openmaic/editor/       #   幻灯片编辑核心
│   ├── @openmaic/importer/     #   PPTX 导入
│   ├── @openmaic/storage/      #   浏览器/HTTP/PostgreSQL/S3 持久化
│   ├── pptxgenjs/              #   定制版 PowerPoint 生成
│   └── mathml2omml/            #   MathML → Office Math 转换
│
├── render-service/             # MP4 视频导出渲染服务（Chromium + FFmpeg，独立容器）
├── skills/                     # 智能体技能包（引导式 SOP）
├── configs/                    # 共享常量（形状、字体、快捷键、主题…）
└── public/                     # 静态资源（Logo、站标、服务商图标）
```

### 关键架构

- **生成流水线**（`@openmaic/generation`）—— 两阶段：大纲生成 → 场景内容生成
- **多智能体编排**（`lib/orchestration/`）—— LangGraph 状态机，管理智能体轮次与讨论
- **回放引擎**（`lib/playback/`）—— 驱动课堂回放与实时互动的状态机
- **动作引擎**（`lib/action/`）—— 执行 28+ 种动作类型（语音、白板绘制/文字/图形/图表、聚光灯、激光笔…）
- **存储层**（`@openmaic/storage`）—— 文档/运行时/素材存储抽象，附 PostgreSQL 参考实现，HTTP 契约可对接外部存储

---

## 10. 开源许可与致谢

### 许可证

本项目基于 [MIT License](LICENSE) 开源，允许免费商用与二次开发。

### 致谢

本项目基于清华大学 THU-MAIC 团队的开源项目 **OpenMAIC**（Open Multi-Agent Interactive Classroom，v1.0.3）二次开发。感谢原团队在多智能体编排、课堂生成、幻灯片引擎与存储层上的开源工作。本项目保留了上游的 MIT 许可证、版权声明与引文信息。

### 第三方组件

仓库内置的以下工作区子包**不**受根目录 MIT 许可证覆盖，各自保留原有协议：

- `packages/mathml2omml` —— [LGPL-3.0-or-later](packages/mathml2omml/LICENSE)
- `packages/pptxgenjs` —— [MIT](packages/pptxgenjs/package.json)（第三方）

整体再分发本仓库时，上述子包内文件适用其各自的协议。

### 上游论文引用

如果上游 OpenMAIC 的工作对你的研究有帮助，请考虑引用：

```bibtex
@Article{JCST-2509-16000,
  title = {From MOOC to MAIC: Reimagine Online Teaching and Learning through LLM-driven Agents},
  journal = {Journal of Computer Science and Technology},
  volume = {},
  number = {},
  pages = {},
  year = {2026},
  issn = {1000-9000(Print) /1860-4749(Online)},
  doi = {10.1007/s11390-025-6000-0},
  url = {https://jcst.ict.ac.cn/en/article/doi/10.1007/s11390-025-6000-0},
  author = {Ji-Fan Yu and Daniel Zhang-Li and Zhe-Yuan Zhang and Yu-Cheng Wang and Hao-Xuan Li and Joy Jia Yin Lim and Zhan-Xin Hao and Shang-Qing Tu and Lu Zhang and Xu-Sheng Dai and Jian-Xiao Jiang and Shen Yang and Fei Qin and Ze-Kun Li and Xin Cong and Bin Xu and Lei Hou and Man-Li Li and Juan-Zi Li and Hui-Qin Liu and Yu Zhang and Zhi-Yuan Liu and Mao-Song Sun}
}
```
