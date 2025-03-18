# 周周黑客松 PPT 生成器

用 AI 和 [Slidev](https://sli.dev/) 快速生成精美活动 PPT，省时高效！

你可以选择从官方的空白模板开始
```bash
pnpm create slidev
```

或者 clone 这个 Git 项目，在这个基础上修改

## 🚀 快速开始

```bash
# 安装依赖
pnpm install

# 启动本地开发服务
pnpm dev

# 构建生产版本
pnpm build

# 导出为 PDF
pnpm export
```

## 📄 项目说明

这个仓库演示了如何通过 AI 辅助的方式快速制作黑客松活动 PPT。整个流程包括：

1. **准备资料**：收集活动信息、社区资料和相关图片
2. **AI 生成**：使用 AI 根据提供的资料生成基础 PPT 内容
3. **微调优化**：针对布局、样式进行微调
4. **部署展示**：部署到线上供访问和使用

## 📁 文件结构

- `prompts/` - 存放活动和社区相关信息
  - `activity.md` - 活动详细信息
  - `community.md` - 社区介绍资料
  - `slidev-template.md` - 完整的 Slidev 生成提示词模板
  - `community-event-template.md` - 社区活动专用简化提示词
  - `mcp-event-sample.md` - MCP 活动示例提示词
- `pages/` - 存放可重用的演示文稿组件
  - `community-intro.md` - 社区介绍模块
  - `feedback.md` - 活动反馈模块
  - `join-community.md` - 参与共创模块
  - `thanks.md` - 感谢页面模块
  - `README.md` - 组件使用说明
- `public/` - 存放图片和静态资源
  - 社区 Logo、活动照片、二维码等
- `slides.md` - 生成的 PPT 主文件

## 🖼️ 图片资源处理

所有图片资源都应放在 `public` 文件夹下，在 slides.md 中引用时使用以下格式：

```markdown
<img src="/logo-cross.png" width="150" />
```

常用图片：
- Logo: `/logo-cross.png`
- 微信公众号二维码: `/wechat_official_qr.jpg"`
- 活动反馈二维码: `/feedback.jpg`
- 活动照片: `/images/events/xxx.jpg`

## 🎨 Slidev 常用布局

- 标准布局: 默认标题和内容布局
- `layout: center`: 内容居中
- `layout: image-right`: 右侧图片布局
- `layout: image-left`: 左侧图片布局
- `layout: two-cols`: 两列布局

## 🧩 模块化组件

该项目使用模块化设计，将常用的社区相关内容提取到 `pages/` 目录下的独立文件中，便于复用和统一管理：

```markdown
---
src: ./pages/community-intro.md
---

# 您的活动特定内容...

---
src: ./pages/feedback.md
---
```

这种模块化方式的优势：
1. **品牌一致性**：社区信息、联系方式等保持一致
2. **便于维护**：更新社区信息只需修改一处
3. **快速创建**：新活动 PPT 可迅速组装核心模块
4. **灵活扩展**：可根据需要创建新的模块或自定义现有模块

详见 `pages/README.md` 了解更多关于模块使用的信息。

## 🔧 自定义调整

PPT 生成后可能需要微调以下内容：

1. 首页 Logo 位置和大小
2. 二维码显示位置
3. 图片路径确保正确
4. 文字大小和布局
5. 配色方案 (通过 CSS 类调整)

## 📱 部署方式

项目已配置好 Netlify 和 Vercel 部署配置文件，可直接部署：

- Netlify: 使用 `netlify.toml`
- Vercel: 使用 `vercel.json`

## 🪄 AI 提示词

可以使用 `prompts/` 目录下的提示词模板生成高质量 Slidev PPT：

- **slidev-template.md**: 完整详细的提示词模板，包含所有自定义选项
- **community-event-template.md**: 社区活动专用简化提示词
- **mcp-event-sample.md**: MCP 活动示例已填写提示词

## 📚 相关资源

- [Slidev 官方文档](https://sli.dev)
- [Slidev 主题](https://sli.dev/themes/gallery.html)
- [Slidev 示例库](https://sli.dev/showcases.html)

## 🤝 贡献

欢迎提交 Issue 或 PR 来完善这个项目！
