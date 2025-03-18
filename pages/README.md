# 社区演示文稿共享组件

这个目录包含周周黑客松社区演示文稿中常用的共享组件。这些组件可以被导入到任何 Slidev 演示文稿中，确保社区品牌和信息的一致性。

## 可用组件

- **community-intro.md** - 社区介绍页面，包含社区基本信息和口号
- **feedback.md** - 活动反馈页面，包含反馈二维码和反馈价值说明
- **join-community.md** - 参与共创页面，包含加入社区的方式和资源
- **thanks.md** - 感谢结束页面，包含社区 Logo 和联系方式

## 使用方法

在主 `slides.md` 文件中，使用 `src` 属性来导入这些共享组件：

```markdown
---
# 其他 Slidev 配置...
---

# 您的活动特定内容...

---
src: ./pages/community-intro.md
---

# 更多活动特定内容...

---
src: ./pages/feedback.md
---

---
src: ./pages/join-community.md
---

---
src: ./pages/thanks.md
---
```

## 自定义

这些共享组件设计为通用模板，您可以根据特定活动需求进行微调：

1. **直接修改源文件** - 如果所有活动都需要相同的更改
2. **复制并修改** - 如果只有特定活动需要不同版本
3. **覆盖内容** - 在导入后添加额外的内容

例如，自定义结束页面的活动特定口号：

```markdown
---
src: ./pages/thanks.md
---

<!-- 覆盖或添加内容 -->
<style>
.custom-message {
  position: absolute;
  top: 60%;
  width: 100%;
  text-align: center;
  font-size: 1.5rem;
  font-weight: bold;
  color: #8b5cf6;
}
</style>

<div class="custom-message">
  您的活动特定口号
</div>
```

## 注意事项

1. 确保所有引用的图片路径保持一致（通常存放在 `/public` 目录）
2. 维护这些共享组件时，考虑向后兼容性
3. 定期更新社区信息，保持最新状态
4. 如果一个组件有多个变体，考虑添加后缀标识（如 `thanks-simple.md`） 