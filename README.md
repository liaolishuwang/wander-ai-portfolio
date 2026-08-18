# Wander AI

Wander AI 是一款 AI 旅行规划产品，将城市、天数、预算和兴趣偏好转化为可执行的多日行程，并通过真实 POI 候选约束提升规划可靠性。

## Android Demo

[下载 Wander AI Android Demo](https://github.com/liaolishuwang/wander-ai-portfolio/releases/download/v2.0.2/Wander-AI-Android-v2.0.2.apk)

- 无需注册或登录即可体验 AI 行程生成。
- 游客行程保存在本地，关闭并重启 App 后仍可恢复。
- APK 为作品集体验版本；Android 安装时可能需要允许浏览器安装未知来源应用。

## 推荐体验路径

1. 打开 App，点击底部中央的“新建行程”。
2. 输入目的地、旅行天数、预算和兴趣偏好。
3. 对比多种行程方案并选择一种。
4. 查看和编辑生成的每日行程。
5. 关闭并重启 App，验证游客行程的本地恢复。

## 核心产品能力

- 根据结构化旅行需求生成多日行程。
- 提供多种方案，帮助用户比较不同旅行风格。
- 使用真实 POI 候选约束地点选择，减少无依据地点。
- 支持行程查看、编辑和持久化。
- 游客无需账号即可体验；正式账号保留云端行程能力。

## AI 规划机制

规划流程结合候选 POI grounding、结构化生成、服务端校验、确定性修复和超时兜底。AI 请求通过受鉴权的服务端入口完成，模型及地图服务密钥不会下发到客户端。

## 30 Case Evaluation

在固定 30 Case 的 Baseline-vs-Current 作品集评测中：

- Final Quality Pass Rate：**26.7% → 100%**
- POI Candidate Hit Rate：**100%**
- Hallucinated POI：**0**
- Current 原始结果中的 **60 次重复核心 POI** 经 deterministic repair 降至 **0**

该结果来自固定 30 Case portfolio evaluation，用于验证当前方案的方向性改进，不代表生产 SLA，也不是统计意义上的通用模型基准。

## 技术栈

React Native · Expo Router · Supabase Auth / Edge Functions · Qwen · 高德 POI · AsyncStorage · EAS Build

## Demo 截图与视频

截图和短视频将在完成隐私检查后补充。

## 当前项目范围

这是面向 AI 产品经理作品集的 Android MVP Demo，重点展示从需求设计、AI 规划链路、安全边界到固定 Case Evaluation 的完整产品闭环。当前公开仓库仅提供项目说明和可安装 APK，不公开完整业务源码、服务端实现、Prompt、原始评测数据或任何密钥。
