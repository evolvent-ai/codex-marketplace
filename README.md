# Evolvent AI Codex Marketplace

公司插件市场，只有目录清单，不保存插件二进制、运行时或凭据。

## 界面添加

打开桌面端 **插件 → 添加市场**，填写 Source `evolvent-ai/codex-marketplace`、Git ref `main`、Sparse paths 留空。
选择 **Evolvent AI**，安装 **Workspace Snapshot**，运行初始化并在设置 → Hooks 信任四项。

## 当前插件

| 插件 | 源仓库 | 路径 |
|---|---|---|
| workspace-snapshot | https://github.com/evolvent-ai/workspace-snapshot | plugins/workspace-snapshot |

两个仓库都是私有的，使用者需要分别有读取权限。添加市场是轻量操作；安装插件时仍需获取完整运行包。

```bash
codex plugin marketplace add evolvent-ai/codex-marketplace --ref main
codex plugin add workspace-snapshot@evolvent-ai
```

新增插件时编辑 `.agents/plugins/marketplace.json` 的 plugins 列表，为独立仓库填写 git-subdir/url 源。
