# 🧭 Jarvis Dynamic Dashboard

实时仪表板，并行从多个数据源获取数据。

## 功能

- 💻 **系统状态** - CPU、内存、磁盘使用率
- 🌤️ **马德里天气** - 实时天气数据
- 📈 **Paper Trading** - 模拟交易账户状态
- 🐙 **GitHub** - OpenClaw 仓库统计
- ⏰ **定时任务** - Cron job 状态

## 技术实现

- **并行数据获取** - 使用 Promise.all 并发获取多个数据源
- **自动更新** - Cron job 每 5 分钟刷新一次
- **实时预览** - 打开 index.html 查看仪表板

## 运行方式

```bash
# 手动更新数据
node update-dashboard.js

# 用浏览器打开
# 直接在浏览器中打开 index.html
```

## 自动更新 (Cron)

数据每 5 分钟自动更新一次。

## 数据源

| 源 | 数据 |
|---|------|
| System | CPU, Memory, Disk via shell |
| Weather | wttr.in API (Madrid) |
| GitHub | GitHub API |
| Trading | Supabase (待实现) |

## 部署

可以部署到 GitHub Pages:
```bash
cd dynamic-dashboard
gh repo create jarvis-dashboard --public
git push -u origin main
```

访问: https://你的用户名.github.io/jarvis-dashboard/
