# 员工安装与使用指南

## 下载

只有 `SKILL_INDEX.md` 标记为已发布且有 GitHub Release 的版本可以下载。当前 Candidate 尚未生成公开 Release。

## Codex 安装

1. 下载目标 Skill 的版本 ZIP，并核对 Release 页面 SHA-256。
2. 解压后确认顶层目录包含 `SKILL.md`、`README.md`、`CHANGELOG.md` 和 `manifest.json`。
3. 将该 Skill 目录复制到个人 Codex Skills 目录；不要覆盖同名历史版本或团队安装副本。
4. 重新打开 Codex，确认 Skill 被识别。
5. 首次使用前阅读状态、权限、依赖和数据边界。

## ChatGPT

ChatGPT 的 Skill/连接器安装机制可能与 Codex 不同。只有 Release README 明确声明并经实测的平台才可使用；否则标记 `UNKNOWN`，不要自行推断兼容。

## 校验 SHA-256

PowerShell：

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath '.\downloaded-skill.zip'
```

结果必须与 Release 页面完全一致。Candidate、UNKNOWN 或未发布包不得作为生产可用 Skill。
