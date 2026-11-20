# Project Workflow Skills

三个面向 Codex 的 Agent Skills，覆盖从接手项目、研发验收到创意成品交付的常见工作。每个 Skill 可独立安装。

Three Chinese-language Agent Skills for project handoff, engineering delivery, and creative production.

| Skill | 适用任务 | 调用示例 |
|---|---|---|
| [项目搭档](skills/project-copilot/SKILL.md) | 盘点多个项目、定位仓库或 worktree、接手已有交付 | 用 `$project-copilot`，确认这个项目该从哪个工作区继续。 |
| [研发交付](skills/project-delivery/SKILL.md) | 实现和修复软件、编排验证、整理验收证据 | 用 `$project-delivery` 修复报告导出，并做本地回归。 |
| [创意制作与交付](skills/creative-delivery/SKILL.md) | 根据素材或模板制作视频、图片、Word 或 PPT，检查导出成品 | 用 `$creative-delivery` 把现有分镜和音轨做成 30 秒预览。 |

## 安装

在 Codex 中发送以下请求。也可以删掉这句话中暂时不需要的 Skill 路径。

> 使用 `$skill-installer`，从 GitHub 仓库 `dassin-alan/project-workflow-skills` 的 `main` 分支安装 `skills/project-copilot`、`skills/project-delivery`、`skills/creative-delivery`。

手动安装时，克隆或下载本仓库，将 `skills/` 下所需的完整 Skill 目录复制到 `$CODEX_HOME/skills`，未设置 `CODEX_HOME` 时使用 `~/.codex/skills`。目录已存在时先保留自己的版本，再对照更新。安装后启动新的 Codex 会话，使用上面的 `$skill-name` 调用。

## 自定义项目地图

如需长期记录自己的项目，在已安装的 `project-copilot/references/` 下复制 [项目地图模板](skills/project-copilot/references/project-map.example.md) 为 `project-map.local.md`，再填写自己的项目路径和交接入口。仓库默认忽略该本地文件。

这三项 Skill 使用文本指令，无需安装运行依赖。具体开发与制作沿用项目工具，也可以调用当前环境中已有的专业 Skill。

[MIT 许可证](LICENSE)
