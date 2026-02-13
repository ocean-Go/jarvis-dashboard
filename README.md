# 🧭 Jarvis Dashboard

实时状态监控面板

## 功能

- 💻 系统状态 - CPU、内存、磁盘
- 🌤️ 马德里天气
- 📈 Paper Trading 账户
- 🐙 GitHub 统计
- 🦞 OpenClaw 状态
- ⏰ 定时任务

## 技术

- 响应式设计，支持手机
- PWA 可安装
- 5 分钟自动刷新

## 在线访问

https://ocean-go.github.io/jarvis-dashboard/

## 本地运行

```bash
cd dynamic-dashboard
python3 -m http.server 3000
# 浏览器打开 http://localhost:3000
```

## 自动更新

数据每 5 分钟通过 cron 更新：
```bash
*/5 * * * * node update-dashboard.js
```
