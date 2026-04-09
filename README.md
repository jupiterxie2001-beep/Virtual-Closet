# VibeCode - AI 穿搭助手

一个现代化的AI穿搭助手应用，帮助用户管理衣橱、生成穿搭方案并进行虚拟试穿。

## 功能特性

- **衣橱管理**：上传衣物照片，自动抠图，手动分类和标记季节
- **智能穿搭方案**：根据天气和风格偏好生成穿搭方案
- **虚拟试穿**：将衣物试穿到参考人物照片上，生成试穿效果
- **人物形象管理**：保存人物形象，方便后续试穿
- **iOS风格UI**：现代化的卡片式布局，美观大方

## 技术栈

- React 19
- TypeScript
- Tailwind CSS
- Lucide React (图标库)
- IndexedDB (本地存储)
- Vite (构建工具)

## 快速开始

### 安装依赖

```bash
npm install
```

### 配置API

创建 `.env.local` 文件并配置以下环境变量：

```env
# 豆包 API 配置
VITE_TRY_ON_ART_API_KEY=your_api_key
VITE_TRY_ON_ART_URL=https://ark.cn-beijing.volces.com/api/v3
VITE_TRY_ON_ART_MODEL=doubao-seedream-4-5-251128
```

### 开发模式

```bash
npm run dev
```

### 构建生产版本

```bash
npm run build
```

### 预览生产版本

```bash
npm run preview
```

## 项目结构

```
src/
├── components/       # 可复用组件
├── pages/           # 页面组件
│   ├── WardrobePage.tsx     # 衣橱页面
│   ├── TryOnPage.tsx       # 试穿页面
│   └── StylistPage.tsx      # 穿搭方案页面
├── agents/          # AI 代理
├── services/        # 服务
├── storage/         # 存储相关
├── types/           # TypeScript 类型定义
└── lib/             # 工具库
```

## 部署说明

### 部署到静态网站托管服务

1. 构建生产版本：`npm run build`
2. 部署 `dist` 目录到以下服务之一：
   - Vercel
   - Netlify
   - GitHub Pages
   - Cloudflare Pages

### GitHub Pages 部署

1. 构建生产版本：`npm run build`
2. 安装 `gh-pages` 包：`npm install --save-dev gh-pages`
3. 添加部署脚本到 `package.json`：
   ```json
   "scripts": {
     "deploy": "gh-pages -d dist"
   }
   ```
4. 运行部署命令：`npm run deploy`

## 功能使用说明

### 1. 管理衣橱

1. 点击“添加衣物”卡片
2. 上传衣物照片
3. 系统会自动抠图并调整大小
4. 手动选择衣物类型和季节
5. 保存到衣橱

### 2. 生成穿搭方案

1. 输入城市名称并获取天气
2. 选择风格偏好
3. 点击“生成穿搭方案”
4. 系统会根据天气和风格从衣橱中选择合适的衣物
5. 点击“去试穿”按钮查看试穿效果

### 3. 虚拟试穿

1. 上传参考人物照片或选择已保存的人物形象
2. 选择要试穿的衣物
3. 点击“生成试穿效果”
4. 系统会调用AI生成试穿效果图
5. 可以点击图片放大查看

## 注意事项

- 本应用使用IndexedDB进行本地存储，数据保存在浏览器中
- 虚拟试穿功能需要配置豆包API密钥
- 首次使用时需要上传一些衣物到衣橱

## 许可证

MIT License
