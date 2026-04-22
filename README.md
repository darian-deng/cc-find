# cc-find

**English** | [中文](#中文说明)

A lightweight CLI tool to globally search your [Claude Code](https://claude.ai/code) session history. Find past conversations by keyword, get the Session ID, and resume right where you left off.

## Install

```bash
sudo curl -fsSL "https://raw.githubusercontent.com/Dengxianyu/cc-find/main/cc-find" \
  -o /usr/local/bin/cc-find && sudo chmod +x /usr/local/bin/cc-find
```

## Usage

```bash
cc-find <keyword>
cc-find <keyword> --limit 50
cc-find <keyword> --all
```

## Update

```bash
cc-find --update
```

The `--update` flag downloads the latest version from GitHub and replaces the installed binary automatically.

## Options

| Flag | Description |
|---|---|
| `--all` | Show all matching sessions (default: 20 most recent) |
| `--limit N` | Show N most recent sessions |
| `--update` | Update to the latest version |
| `--version` | Print current version |

## Resume a Session

```bash
claude --resume <session-id>
```

## Requirements

- Python 3.6+
- macOS or Linux
- [Claude Code](https://claude.ai/code) installed (creates `~/.claude/`)

---

<a name="中文说明"></a>

# cc-find 中文说明

**[English](#cc-find)** | 中文

轻量级命令行工具，全局搜索 [Claude Code](https://claude.ai/code) 的历史会话记录。通过关键词找到过去的对话，获取 Session ID，随时恢复继续。

## 安装

```bash
sudo curl -fsSL "https://raw.githubusercontent.com/Dengxianyu/cc-find/main/cc-find" \
  -o /usr/local/bin/cc-find && sudo chmod +x /usr/local/bin/cc-find
```

## 使用方法

```bash
cc-find <关键词>
cc-find <关键词> --limit 50   # 显示最近 50 条
cc-find <关键词> --all         # 显示全部结果
```

## 更新

```bash
cc-find --update
```

`--update` 会自动从 GitHub 拉取最新版本并替换本地已安装的文件，无需重新执行安装命令。

## 参数说明

| 参数 | 说明 |
|---|---|
| `--all` | 显示全部匹配会话（默认只显示最近 20 条）|
| `--limit N` | 显示最近 N 条会话 |
| `--update` | 更新到最新版本 |
| `--version` | 查看当前版本号 |

## 恢复会话

```bash
claude --resume <session-id>
```

将搜索结果中的 Session ID 粘贴到上面的命令中，即可在 Claude Code 中恢复对应的历史对话。

## 运行环境

- Python 3.6+
- macOS 或 Linux
- 已安装 [Claude Code](https://claude.ai/code)（会在 `~/.claude/` 下生成会话文件）
