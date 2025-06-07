# 📚 HTML技术文档库

一个优雅的HTML技术文档管理和展示系统，专门用于管理企业级技术方案和开发文档。

## 🌟 项目特点

- 📱 **响应式设计** - 完美适配桌面和移动设备
- 🔍 **智能搜索** - 支持文档标题和内容搜索
- 🎨 **现代化UI** - 采用Tailwind CSS，界面美观简洁
- 🚀 **快速部署** - 支持Vercel、Netlify等平台一键部署
- 📦 **模块化管理** - 每个文档独立管理，便于维护

## 📋 当前文档列表

### 1. Java技术文档
- **JDK 8 vs JDK 21 交互式探索** ☕
  - 深入对比JDK 8与JDK 21的新特性和改进
  - 提供实际代码示例和性能对比
  - 更新日期：2025-06-01

### 2. 企业级API集成方案
- **华熙生物关务系统与DHL API对接方案** 🚀
  - 完整的企业级API对接技术方案
  - 包含运单管理和DPS申报功能的Java实现
  - 基于DHL官方文档验证和完善
  - 提供详细的代码示例和部署指南
  - 更新日期：2025-06-07

## 🚀 快速开始

### 本地运行

```bash
# 克隆仓库
git clone https://github.com/yak33/html-docs.git

# 进入项目目录
cd html-docs

# 使用任意HTTP服务器运行（例如Python）
python -m http.server 8000

# 或使用Node.js
npx serve .

# 在浏览器中访问
open http://localhost:8000
```

### 在线访问

🌐 **演示地址**: [https://your-domain.vercel.app](https://your-domain.vercel.app)

## 📁 项目结构

```
html-docs/
├── index.html                                    # 主索引页面
├── JDK 8 vs JDK 21 交互式探索.html              # Java技术对比文档
├── 华熙生物关务系统与DHL API对接方案.html         # 企业API集成方案
├── 方案用资料/                                   # 参考资料目录
│   ├── DPS DECLARATION API v1.2.7.docx          # DHL DPS API文档
│   ├── MyDHL API 接口开发手册_REST专用_202203.pdf # MyDHL API手册
│   ├── MyDHL API Request body 中文说明_REST专用.xlsx # API参数说明
│   ├── Parcel_PLT Service with DHL invoice_Request.txt # 请求示例
│   ├── Parcel_PLT Service with DHL invoice_Response.txt # 响应示例
│   ├── Test cases_新版MyDHL API.txt              # 测试用例
│   ├── 在线申报接口使用指南_v1.3.pdf              # 申报接口指南
│   └── readme.md                                 # 资料说明
└── README.md                                     # 项目说明文档
```

## 🛠️ 技术栈

- **前端框架**: 原生HTML5 + CSS3 + JavaScript
- **CSS框架**: [Tailwind CSS](https://tailwindcss.com/) (CDN)
- **图标**: Unicode Emoji + SVG图标
- **部署**: 支持静态托管服务（Vercel、Netlify、GitHub Pages等）

## 📝 添加新文档

### 方法1: 直接添加HTML文件

1. 将新的HTML文档放入项目根目录
2. 在 `index.html` 中更新 `htmlFiles` 数组：

```javascript
const htmlFiles = [
    // 现有文档...
    {
        name: "新文档.html",
        title: "新文档标题",
        date: "2025-06-07",
        description: "文档描述信息"
    }
];
```

### 方法2: 使用Git提交

```bash
# 添加新文档
git add 新文档.html
git add index.html  # 如果更新了索引

# 提交更改
git commit -m "feat: 添加新技术文档"

# 推送到远程仓库
git push origin master
```

## 🎯 文档编写规范

### HTML文档标准

- ✅ 使用UTF-8编码
- ✅ 包含完整的HTML5文档结构
- ✅ 响应式设计，支持移动端
- ✅ 添加适当的meta标签
- ✅ 使用语义化HTML标签

### 推荐模板结构

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>文档标题</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- 自定义样式 -->
</head>
<body>
    <div class="max-w-4xl mx-auto p-8">
        <h1>文档标题</h1>
        <!-- 文档内容 -->
    </div>
</body>
</html>
```

## 🔧 配置说明

### 图标识别规则

文档会根据文件名自动分配图标：

- ☕ **Java相关**: `java`, `JDK`
- ⚛️ **前端框架**: `vue`, `react`
- 🎨 **样式相关**: `css`, `style`
- 📜 **JavaScript**: `js`, `javascript`
- 🚀 **API对接**: `API对接`, `DHL`, `华熙生物`
- 📦 **物流相关**: `关务`, `物流`
- 📄 **默认文档**: 其他类型

### 搜索功能

- 支持按文档标题搜索
- 支持按文档描述搜索
- 实时搜索，无需刷新页面
- 键盘快捷键：`Ctrl + /` 快速聚焦搜索框

## 🚀 部署指南

### Vercel部署

1. Fork此仓库到你的GitHub账号
2. 在[Vercel](https://vercel.com)中导入项目
3. 配置部署设置（通常无需特殊配置）
4. 点击Deploy即可完成部署

### GitHub Pages部署

1. 在仓库Settings中找到Pages选项
2. 选择Source为"Deploy from a branch"
3. 选择branch为"master"，folder为"/ (root)"
4. 保存设置，等待部署完成

### Netlify部署

1. 在[Netlify](https://netlify.com)中连接GitHub仓库
2. 选择要部署的分支（通常是master）
3. 构建设置保持默认即可
4. 点击"Deploy site"完成部署

## 🤝 贡献指南

欢迎提交新的技术文档或改进现有文档！

1. **Fork** 此仓库
2. **创建特性分支** (`git checkout -b feature/新功能`)
3. **提交更改** (`git commit -m 'feat: 添加新功能'`)
4. **推送到分支** (`git push origin feature/新功能`)
5. **提交Pull Request**

### 提交信息规范

请使用以下格式：

- `feat:` 新功能
- `fix:` 修复Bug
- `docs:` 文档更新
- `style:` 代码格式调整
- `refactor:` 代码重构
- `chore:` 构建/工具相关

## 📜 许可证

MIT License - 详见 [LICENSE](LICENSE) 文件

## 📞 联系方式

- **项目维护者**: [yak33](https://github.com/yak33)
- **GitHub**: https://github.com/yak33/html-docs
- **Issues**: [提交问题](https://github.com/yak33/html-docs/issues)

## 🙏 致谢

- [Tailwind CSS](https://tailwindcss.com/) - 优秀的CSS框架
- [DHL Developer Portal](https://developer.dhl.com/) - API文档参考
- 所有贡献者和文档作者

---

<div align="center">
  <p>⭐ 如果这个项目对你有帮助，请给个Star支持一下！</p>
  <p>🚀 Made with ❤️ by <a href="https://github.com/yak33">yak33</a></p>
</div>

