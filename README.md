# 💡 IdeaPod (需求豆)

**IdeaPod** 是一款专为高效工作流设计的轻量级 macOS 菜单栏（MenuBar）应用。它致力于解决日常工作中“需求收集繁琐、灵感容易遗忘”的痛点。

通过 IdeaPod，你可以随时通过全局快捷键唤起输入框，将用户反馈或产品灵感极速捕获，并**全自动结构化地同步至飞书多维表格（Bitable）**，实现“即用即走，无缝流转”。

---

## ✨ 核心特性

- **⚡️ 极速唤起与提交**
  - 驻留于系统菜单栏，随时点击或通过全局快捷键唤起。
  - 支持 `Cmd + Enter` 一键快捷提交，表单即刻清空，无缝衔接当前工作。
  
- **🔄 飞书多维表格无缝对接**
  - **动态选项拉取**：应用初始化时，自动拉取飞书表格中的【迭代版本】选项。
  - **结构化录入**：支持填写需求名称、详细内容、负责人，并可快速切换优先级（P0-高 / P1-中 / P2-低）。
  - **状态自动流转**：需求提交后，在飞书中自动标记为“待讨论”状态。

- **📎 原生附件上传**
  - 支持直接拖拽或点击上传本地图片、截图及文档。
  - 后台自动完成“飞书文件上传 -> Token 换取 -> 多维表格关联”的全链路处理。

- **🛡️ 零阻塞体验**
  - 采用异步静默提交机制，附带 Loading 与 Toast 状态提示，网络请求不卡顿、不影响你的连续输入。

---

## 🚀 安装与运行指南

由于当前版本为内部测试分发版，安装时请遵循以下步骤：

### 1. 下载应用
进入 [Releases 页面](https://github.com/Bandit-A/idelPod/releases/tag/TestGame)下载最新版本的 `IdeaPod.zip` 并解压，将 `IdeaPod.app` 拖入你的 **应用程序 (Applications)** 文件夹。

### 2. 首次运行与权限放行 (重要)
由于 macOS 的 Gatekeeper 安全机制，首次打开从 GitHub 下载的应用可能会提示“无法验证开发者”。请按以下步骤操作：

- **方法一（推荐）**：在 Finder 中找到 `IdeaPod.app`，**按住键盘 `Control` 键**，用鼠标**右键点击**应用图标，选择**“打开”**。在弹出的确认框中点击**“仍要打开”**即可。（此操作只需执行一次，后续可直接双击打开）。
- **方法二**：若提示“文件已损坏”，请打开 Mac 自带的「终端 (Terminal)」应用，运行以下命令解除安全隔离：
  ```bash
  xattr -cr /Applications/IdeaPod.app

### 3. 前期准备 (Feishu Setup Guide)
## ⚙️ 飞书端准备

在正式使用 IdeaPod 前，你需要先在飞书端完成相关的应用与权限配置。整个流程如下：

```mermaid
flowchart TD
    A([1. 引入多维表格模板https://jvx5ghwlv9j.feishu.cn/base/MnqcbBx83aYbP2stbc6cVOV5nBf?from=from_copylink]) --> B([2. 开放平台创建飞书应用])
    B --> C([3. 开通编辑与附件上下传权限])
    C --> D([4. 将应用机器人加为表格协作者])
    D --> E([5. 设置机器人权限为可编辑])

## ⚙️ 应用端准备
    E --> F([6. 在 IdeaPod 填写各项配置])

    
    style A fill:#e1f5fe,stroke:#03a9f4,stroke-width:2px
    style B fill:#e1f5fe,stroke:#03a9f4,stroke-width:2px
    style C fill:#e1f5fe,stroke:#03a9f4,stroke-width:2px
    style D fill:#e1f5fe,stroke:#03a9f4,stroke-width:2px
    style E fill:#e1f5fe,stroke:#03a9f4,stroke-width:2px
    style F fill:#e8f5e9,stroke:#4caf50,stroke-width:2px

