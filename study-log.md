# 学习日志

分支 `study/notes`，用于记录阅读 BMAD-METHOD 源码的过程。
基线提交：`bda3c592`（2026-10-06，docs(skills): state the render command's outcomes plainly in SKILL.md）。

模板：每天一段，写「读了什么 / 关键概念 / 未解决的疑问 / 下一步」。

---

## 2026-10-11 仓库初探

**环境**
- fork 自 `bmad-code-org/BMAD-METHOD`，本地 `origin` = `sunrong1/BMAD-METHOD`；尚未配置 `upstream`。
- 本地仅有 `main` 分支，无 `dev`（`AGENTS.md` 要求 PR 从 `dev` 出发并合回 `dev`）。
- 校验命令 `uv run tools/validate_skills.py --strict` 通过：33 个 skill，0 问题。

**结构**
- `skills/`：33 个 skill，`bmad-*`（方法侧）与 `bmod-*`（模块侧）；`bmad-toolsmith/` 最大（88 文件），`bmad/` 含 21 个 py。
- `tools/`：Python 工具（`validate_skills.py`、`dogfood.py`…）与规则文档（`skill-validator.md`、`ticket-tree-rules.md`…）。
- `docs/`（192 篇 md）+ `docs-site/`（Astro 站点）。

**待验证**
- 本 fork 是否已有自有改动（无 upstream 引用，暂无法 diff）。
- skill 的 `SKILL.md` / `workflows/` / 配置文件的标准形态与加载机制。
