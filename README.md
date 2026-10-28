# Speak Atlas — Netlify 静态部署版

这是一个可直接部署到 Netlify 的英语单词学习网站原型，包含今日学习、词汇星图、单词搜索、简单选择题、发音（浏览器语音合成）、本地学习进度和深浅主题切换。

## 部署
1. 将整个项目文件夹上传到你自己的 GitHub 仓库。
2. 在 Netlify 选择 **Add new project → Import an existing project**，连接该 GitHub 仓库。
3. Build command 留空，Publish directory 填 `.`。仓库中的 `netlify.toml` 也已设置发布目录。
4. 点击 Deploy。

也可以在 Netlify 中直接拖放整个项目文件夹进行手动部署（如需后续自动更新，建议使用 GitHub 连接部署）。

## 文件
- `index.html` 页面结构
- `style.css` 响应式样式
- `app.js` 搜索、复习、发音、主题与本地进度逻辑
- `assets/words.json` 示例词库数据
- `netlify.toml` Netlify 配置

## 重要说明
- 这是独立制作的相似风格原型，不是 `speak.is` 的原始源码，也不保证与其像素级一致。
- 为避免假称完整复刻，本压缩包没有包含 Word Atlas 的 7,298 条词汇、插画与音频资产；内置少量示例词条用于演示。可在 `app.js` 的 `words` 数组中继续添加内容。
- 学习记录保存在当前浏览器的 `localStorage`，不是云同步；清除浏览器数据可能导致记录丢失。
- 发音使用浏览器内置语音合成，具体音色取决于设备和浏览器。
