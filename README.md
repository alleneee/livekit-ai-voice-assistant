# AI 语音助手项目

基于 LiveKit 实现的实时AI语音助手系统。

## 项目概述

本项目是一个基于 LiveKit 实现的实时AI语音助手系统,支持语音识别、实时对话等功能。项目采用前后端分离架构,提供流畅的用户体验和强大的AI对话能力。

## 系统架构

### 整体架构

项目采用前后端分离架构:

```
AI语音助手
├── 前端 (Next.js)
│   ├── 用户界面
│   ├── 实时音频流处理
│   └── WebRTC 通信
└── 后端 (Python)
    ├── LiveKit 服务
    ├── 语音识别 (Deepgram)
    └── AI对话 (OpenAI)
```

### 技术栈

#### 后端技术栈

- 主框架: Python
- 实时通信: LiveKit SDK
- 语音识别: Deepgram API
- AI对话: OpenAI API
- 环境管理: venv

#### 前端技术栈

- 框架: Next.js
- 开发语言: TypeScript
- UI框架: Tailwind CSS
- 实时通信: LiveKit Client SDK
- 包管理: pnpm

## 核心功能

1. 实时语音识别
2. AI实时对话
3. 低延迟音频传输
4. 响应式用户界面

## 项目结构

```
项目根目录
├── backend/                # 后端代码
│   ├── agent.py           # 主要业务逻辑
│   ├── requirements.txt   # Python依赖
│   └── docs/             # 后端文档
│
└── front/                 # 前端代码
    ├── app/              # Next.js应用
    ├── components/       # UI组件
    └── public/          # 静态资源
```

## 环境配置

### 后端配置

需要在 `.env.local` 中配置以下环境变量:

- LIVEKIT_URL
- LIVEKIT_API_KEY
- LIVEKIT_API_SECRET
- OPENAI_API_KEY
- DEEPGRAM_API_KEY

### 前端配置

需要在 `.env.local` 中配置以下环境变量:

- NEXT_PUBLIC_LIVEKIT_URL
- LIVEKIT_API_KEY
- LIVEKIT_API_SECRET

## 开发指南

### 后端开发

1. 创建虚拟环境:
```bash
python3 -m venv venv
source venv/bin/activate
```

2. 安装依赖:
```bash
pip install -r requirements.txt
```

3. 启动服务:
```bash
python3 agent.py dev
```

### 前端开发

1. 安装依赖:
```bash
pnpm install
```

2. 启动开发服务器:
```bash
pnpm dev
```

## 部署指南

1. 后端部署
   - 确保Python环境 >= 3.8
   - 配置所需的环境变量
   - 使用生产级别的WSGI服务器

2. 前端部署
   - 构建生产版本: `pnpm build`
   - 部署到静态托管服务
   - 配置环境变量

## 许可证

本项目基于 MIT 许可证开源。