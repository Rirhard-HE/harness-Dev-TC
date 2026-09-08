# harness-Dev-TC

面向 Codex / ChatGPT 桌面端的 AI 产品交付 Harness。仓库保存基础工作章程、项目入口和跨设备迁移说明。

## 克隆后使用

```bash
git clone https://github.com/Rirhard-HE/harness-Dev-TC.git
cd harness-Dev-TC
codex
```

从仓库根目录启动新的 Codex 会话。Codex 会自动读取根目录的 `AGENTS.md`。该文件已包含基础 Harness 核心规则和项目入口，不依赖设备上预先存在的 `~/.codex/AGENTS.md`。

可以在新会话中执行：

```text
请列出当前加载的指令来源，并概括本项目的任务分级、上下文分级、授权、Memory 和验收规则。
```

## 当前仓库内容

- `AGENTS.md`：可随仓库迁移的自包含基础规则。
- `Harness-跨设备迁移与重建手册-V1.0.md`：迁移、重建和验收规范。
- `README.md`：克隆与验证说明。

## 当前边界

克隆本仓库可以恢复基础规则，但以下内容尚未进入仓库，因此不能宣称完整 Harness 已恢复：

- 原项目的 `memory/00` 至 `09`；
- `reasoning-review-memory` 自定义 Skill；
- 插件安装状态和第三方账号授权；
- Hooks、设备配置、API Key、Cookie、Token和登录态；
- 原项目附件、截图、代码和完整业务上下文。

这些内容必须按迁移手册分阶段恢复。不得将 `config.toml`、`auth.json`、缓存、会话目录或任何凭证提交到仓库。

## 恢复状态

- 阶段 A：仓库与当前在线环境只读盘点已完成。
- 阶段 B：基础规则已写入；MIG-001 至 MIG-005 静态验收通过。
- 动态验收：需要从仓库根目录启动一个新的 Codex 运行。
- 阶段 C 至 F：尚未执行。
