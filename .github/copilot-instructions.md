## 快速背景（为 AI 代码代理准备）

- 本仓库名为 `Telegram-Gift-Parser`，README 描述这是一个用 Python 编写的 Telegram 礼物/抽奖抓取器（示例命令：`pip install -r requirements.txt`、`python main.py`），并展示了 `config.json` 的典型键：`api_key`、`channels`、`notification`。
- 注意：仓库根目录当前存在 `main.cpp`，其内容是 git 提交命令（看起来像占位/错误），并不是可运行的 C++ 源码。对任何自动修改或构建前，请先确认仓库的实际语言/入口文件（是否存在 `main.py`、`requirements.txt`、`config.json`）。

## 你的目标（要点）

- 帮助维护者把 README 中描述的 Python 工具保持可运行：优先查找 `main.py`、`requirements.txt`、`config.json` 和 releases 里的可执行包。若这些文件缺失或与 README 不符，请创建 issue 或 PR 报告差异。
- 在变更中避免破坏 releases、LICENSE 或 README；保留现有发布/分发文件。

## 可操作规则（短）

1. 首先扫描并引用下列文件/位置以获取上下文：`README.md`, 根目录（查找 `main.py`, `requirements.txt`, `config.json`）, `main.cpp`（注意其异常内容）, `LICENSE`, GitHub Releases 页面。
2. 当 README 与仓库内容不一致时：
   - 在变更 PR 描述中明确记录不一致处（举例：README 要求 `python main.py`，但仓库缺少 `main.py`）。
   - 若变更能修复差异（例如添加缺失的 `main.py` 或更新 README），请同时添加说明并将测试/运行步骤写入 README。
3. 对配置约定的处理：遵循 README 中展示的 `config.json` 字段（`api_key`, `channels`, `notification`），修改涉及这些字段时保持向后兼容，或在 README 中清晰记录迁移步骤和示例。
4. 不要擅自删除 `main.cpp`——它当前看起来像占位或误提交；若你要清理它，请在 PR 中解释原因并保留历史证明（或移动到 `archive/` 而非直接删除）。

## 示例片段（可直接引用）

- README 指令示例：

  - 安装依赖（来自 README）：`pip install -r requirements.txt` — 确认 `requirements.txt` 是否存在。
  - 运行入口（来自 README）：`python main.py` — 如果仓库没有 `main.py`，请优先定位入口文件或在 PR 中添加。

## 合并与 PR 建议

- 提交信息应清晰说明修复或变更目的（例："fix: add main.py to match README; add minimal config example"）。
- 若变更会影响用户运行方式（例如要求新的依赖、不同的配置键名），请在 PR 中更新 README 并提供迁移示例。

## 不要做的事（禁忌）

- 不要假设项目运行在 C++：当前 `main.cpp` 的内容可疑，不要直接用它替换 README 中的 Python 说明。
- 不要在没有认证的情况下公开或编码任何真实的 Telegram API 密钥；在示例中使用占位符（`YOUR_TELEGRAM_API_KEY`）。

## 如果信息不足（决策准则）

- 优先级：保证 README 的准确性 > 添加新功能 > 重构。若不确定，提出 issue 并在 PR 中标注 "needs maintainer confirmation"。

---

如果你希望我根据仓库中更多文件（例如实际的 `main.py`、`requirements.txt` 或 `config.json`）补充示例和运行步骤，告诉我我将继续查找并更新本文件。
