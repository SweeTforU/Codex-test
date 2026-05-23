# Codex-test: 贪吃蛇（Snake）

这是一个纯前端、单文件（`index.html`）的贪吃蛇小游戏，支持：

- 手机触控：方向键（D-pad）+ 滑动
- 桌面键盘：方向键 / WASD
- 暂停 / 继续、重新开始
- 奖励食物、等级加速、最高分本地存储

## 本地运行

直接用浏览器打开 `index.html` 即可。

## Git 目录基础初始化说明

本仓库补充了基础的 `.gitignore`，用于排除不应进入版本库的内容（例如编辑器配置、日志、临时文件、依赖目录、环境变量文件等），保持仓库干净、可复现、便于协作。

## 分支策略（已切换为 `main` 主分支）

当前策略改为：

- `main`：主分支，作为默认入口。
- `topic/*`：按任务创建临时分支，任务名直接写在分支名里，方便辨别。

命名示例：

- `topic/snake-game`（贪吃蛇）
- `topic/todo-app`（待办应用）
- `topic/api-auth`（接口鉴权）

推荐流程：

1. 从 `main` 拉出任务分支：`git checkout -b topic/<task-name> main`
2. 在任务分支开发并提交
3. 完成后合并回 `main`

这样可以兼顾两点：

1. `main` 始终是主线，不会找不到当前主分支。
2. 不同方向代码不会混在一个长期分支里，后续回看和回滚都更清晰。

## 常见提示：什么是“分支领先 / 需要拉取或合并”

在 `git status` 中常见三种状态：

- ahead（领先）：本地分支比远端多提交，执行 `git push` 即可。
- behind（落后）：远端分支有新提交，本地没有，先执行 `git pull`。
- diverged（分叉）：本地和远端都有新提交，先 `git pull --rebase`（或 merge）解决后再 `git push`。

推荐日常顺序：

1. `git status -sb`
2. `git pull --rebase`（如需要）
3. `git push`
