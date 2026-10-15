# open-claude-ui-SafeFork

这是 [Caho1/open-claude-ui](https://github.com/Caho1/open-claude-ui) 的 SafeFork。

- [main](https://github.com/CaptainUnhappy/open-claude-ui-SafeFork/tree/main)：上游源码和原始 Git 历史，保留上游 [MIT 许可证](https://github.com/CaptainUnhappy/open-claude-ui-SafeFork/blob/main/LICENSE)。
- `sync-control`：默认控制分支，仅保存安全同步工作流和说明。

## 同步规则

- 计划每小时检查上游全部分支和标签；GitHub 定时运行可能延迟或跳过。
- 只新增缺失引用、快进更新分支；不合并、不强推、不删除已有引用，也不创建自动备份分支。
- 上游不可访问、分支历史分叉或未经审核的标签冲突时停止，保留 Fork 现状。
- 同步使用短期 `GITHUB_TOKEN`，不依赖长期写入密钥；默认仅启用 Safe Fork Sync。
- 只同步 Git 分支和标签，不复制 Releases、发布附件、Issues、Actions 历史或 Git LFS 对象。

可在 [Safe Fork Sync](https://github.com/CaptainUnhappy/open-claude-ui-SafeFork/actions/workflows/safe-fork-sync.yml) 查看记录或手动运行；选择 `dry_run` 仅检查、不写入。

完整规则见 [SafeFork 规范](https://github.com/CaptainUnhappy/SafeFork/blob/main/skills/safefork/references/spec.md)。控制分支的同步工作流采用 [MPL-2.0](LICENSE)，不改变上游源码许可证。
