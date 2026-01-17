# ZQ-TV - 免费在线视频搜索与播放平台

<div align="center">
  <img src="https://images.icon-icons.com/38/PNG/512/retrotv_5520.png" width="120">
  <br>
  <p><strong>自由观影，畅享精彩</strong></p>
</div>

---

## 📺 项目简介

ZQ-TV 是一个开源、轻量级的在线视频搜索与播放平台，聚合多个视频源，支持多端访问，无需注册即可使用。前端纯静态，后端支持 Cloudflare Pages Functions 代理，安全无广告，体验流畅。

---

## 🚀 快速部署（推荐 Cloudflare Pages）

1. Fork 或下载本仓库到你的 GitHub 账户
2. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com/)，进入 Pages
3. 新建项目，连接你的 GitHub 仓库
4. 构建命令留空，输出目录留空（默认根目录）
5. 部署即可上线
6. （可选）在"设置" > "环境变量"添加 `PASSWORD` 实现访问密码保护

> 也支持 Vercel、Netlify 等平台部署，方法类似。

---

## 🔧 主要功能

- 多视频源聚合搜索与播放
- 支持自定义 API 源，兼容苹果CMS V10标准
- 支持 Cloudflare Functions 代理，突破跨域限制
- 密码保护（环境变量设置）
- 广告过滤、成人内容过滤
- 观看历史、进度记忆
- 响应式设计，适配手机/平板/PC
- PWA 支持，可添加到桌面

---

## 🛠️ 技术栈

- HTML5 + CSS3 + JavaScript (ES6+)
- Tailwind CSS（CDN）
- DPlayer + HLS.js
- Cloudflare Pages Functions（Serverless 后端）
- localStorage 本地存储

---

## ⚙️ 自定义配置

### 密码保护
- 在部署平台设置环境变量 `PASSWORD`，即可开启访问密码。

### 添加自定义 API
- 在设置面板选择"自定义接口"，填写你的苹果CMS兼容 API 域名即可。
- 搜索接口示例：`https://example.com/api.php/provide/vod/?ac=videolist&wd=关键词`
- 详情接口示例：`https://example.com/api.php/provide/vod/?ac=detail&ids=视频ID`

---

## ⌨️ 播放器快捷键

- 空格：播放/暂停
- 左右箭头：快退/快进
- 上下箭头：音量调节
- M：静音
- F：全屏
- Esc：退出全屏

---



- GitHub Issues 欢迎提问与建议
- 欢迎 Star & Fork！


