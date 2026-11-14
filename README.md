# arrake's Scoop Bucket

个人开源桌面与命令行工具的 [Scoop](https://scoop.sh) 声明式软件源。

## 快速使用

```powershell
# 1. 添加软件源
scoop bucket add arrake https://github.com/arrake0101/scoop-bucket

# 2. 安装软件
scoop install arrake/mailchat
```

### 在 `scoopfile.json` 中声明式管理

```json
{
  "buckets": [
    {
      "Name": "arrake",
      "Source": "https://github.com/arrake0101/scoop-bucket"
    }
  ],
  "apps": [
    {
      "Name": "mailchat",
      "Source": "arrake"
    }
  ]
}
```

## 已收录应用

| 应用 | 说明 | 安装命令 |
| :--- | :--- | :--- |
| [**mailchat**](https://github.com/arrake0101/mailchat) | 把标准邮箱做成现代即时通讯桌面客户端（IMAP/SMTP 单聊与全员群聊 + Agent 声明式 `config.toml` + DPAPI 凭据隔离） | `scoop install arrake/mailchat` |

## 自动追更机制

本仓库内置 `.github/workflows/excavator.yml` 自动巡检工作流（基于官方 `ScoopInstaller/GithubActions`），无需配置任何跨仓库密钥，自动对比上游 GitHub Releases 最新版本与 `SHA256SUMS.txt` 并提交清单更新；也可在 Actions 页面手动一键触发立即同步。
