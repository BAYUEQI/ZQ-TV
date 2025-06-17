# ZQ-TV - 免费在线视频搜索与观看平台

<div align="center">
  <img src="https://images.icon-icons.com/38/PNG/512/retrotv_5520.png" alt="LibreTV Logo" width="120">
  <br>
  <p><strong>自由观影，畅享精彩</strong></p>
</div>

## 📺 项目简介

ZQ-TV 是一个轻量级、免费的在线视频搜索与观看平台，提供来自多个视频源的内容搜索与播放服务。无需注册，即开即用，支持多种设备访问。项目结合了前端技术和后端代理功能，可部署在支持服务端功能的各类网站托管服务上。

本项目基于 [bestK/tv](https://github.com/bestK/tv) 进行重构与增强。

<details>
  <summary>点击查看项目截图</summary>
  <img src="https://github.com/user-attachments/assets/df485345-e83b-4564-adf7-0680be92d3c7" alt="项目截图" style="max-width:600px">
</details>

## 📋 详细部署指南

### Cloudflare Pages

1. Fork 或克隆本仓库到您的 GitHub 账户
2. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com/)，进入 Pages 服务
3. 点击"创建项目"，连接您的 GitHub 仓库
4. 使用以下设置：
   - 构建命令：留空（无需构建）
   - 输出目录：留空（默认为根目录）
5. 点击"保存并部署"
6. 可选：在"设置" > "环境变量"中配置密码保护

### Vercel

1. Fork 或克隆本仓库到您的 GitHub/GitLab 账户
2. 登录 [Vercel](https://vercel.com/)，点击"New Project"
3. 导入您的仓库，使用默认设置
4. 点击"Deploy"
5. 可选：在"Settings" > "Environment Variables"中配置密码保护

### Netlify

1. Fork 或克隆本仓库到您的 GitHub 账户
2. 登录 [Netlify](https://app.netlify.com/)
3. 点击"New site from Git"，选择您的仓库
4. 构建设置保持默认
5. 点击"Deploy site"
6. 可选：在"Site settings" > "Build & deploy" > "Environment"中配置密码保护




## 🔧 自定义配置

### 密码保护

要为您的 ZQ-TV 实例添加密码保护，可以在部署平台上设置环境变量：

**环境变量名**: `PASSWORD` 
**值**: 您想设置的密码

各平台设置方法：

- **Cloudflare Pages**: Dashboard > 您的项目 > 设置 > 环境变量
- **Vercel**: Dashboard > 您的项目 > Settings > Environment Variables
- **Netlify**: Dashboard > 您的项目 > Site settings > Build & deploy > Environment
- **Docker**: 使用 `-e PASSWORD=your_password` 参数

### API兼容性

LibreTV 支持标准的苹果 CMS V10 API 格式。添加自定义 API 时需遵循以下格式：
- 搜索接口: `https://example.com/api.php/provide/vod/?ac=videolist&wd=关键词`
- 详情接口: `https://example.com/api.php/provide/vod/?ac=detail&ids=视频ID`

**添加 CMS 源**:
1. 在设置面板中选择"自定义接口"
2. 接口地址只需填写到域名部分: `https://example.com`（不要包含`/api.php/provide/vod`部分）

## ⌨️ 键盘快捷键

播放器支持以下键盘快捷键：

- **空格键**: 播放/暂停
- **左右箭头**: 快退/快进
- **上下箭头**: 音量增加/减小
- **M 键**: 静音/取消静音
- **F 键**: 全屏/退出全屏
- **Esc 键**: 退出全屏

## 🛠️ 技术栈

- HTML5 + CSS3 + JavaScript (ES6+)
- Tailwind CSS (通过 CDN 引入)
- HLS.js 用于 HLS 流处理
- DPlayer 视频播放器核心
- Cloudflare/Vercel/Netlify Serverless Functions
- 服务端 HLS 代理和处理技术
- localStorage 本地存储

## 🔄 更新日志

<details>
  <summary>点击查看更新日志</summary>

- **1.1.2** (2025-04-22): 新增豆瓣热门内容显示，设置中可开关
- **1.1.1** (2025-04-19): 
  - 修复 docker 部署时无法搜索的问题
  - 修复播放页面进度保存与恢复的兼容性问题  
- **1.1.0** (2025-04-17): 添加服务端代理功能，支持 HLS 流处理和解析，支持环境变量设置访问密码
- **1.0.3** (2025-04-13): 性能优化、UI优化、更新设置功能
- **1.0.2** (2025-04-08): 分离播放页面，优化视频源 API 兼容性
- **1.0.1** (2025-04-07): 添加广告过滤功能，优化播放器性能
- **1.0.0** (2025-04-06): 初始版本发布

</details>


