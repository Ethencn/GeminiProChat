# 马里奥风格游戏使用指南

## 游戏简介

这是一个经典的2D横版平台跳跃游戏，玩法类似超级马里奥。

### 游戏特性
- 🎮 经典的平台跳跃玩法
- ⬅️➡️ 流畅的角色移动控制
- 🚀 真实的跳跃物理系统
- 👾 会巡逻的敌人AI
- 🪙 金币收集系统
- 🏆 多关卡设计
- ❤️ 生命系统

### 游戏操作
- **⬅️ 左方向键** - 向左移动
- **➡️ 右方向键** - 向右移动
- **空格键** - 跳跃
- **R键** - 重新开始游戏

### 游戏规则
1. 收集所有金币即可进入下一关
2. 从上方跳到敌人头上可消灭敌人并获得100分
3. 从侧面碰到敌人会失去一条生命
4. 掉出屏幕底部会失去一条生命
5. 生命耗尽游戏结束

## 如何运行游戏

### 方法1：本地运行（开发环境）

**前置要求：**
- Node.js v18 或更高版本
- pnpm 包管理器

**步骤：**

1. **克隆仓库**
   ```bash
   git clone https://github.com/Ethencn/GeminiProChat.git
   cd GeminiProChat
   ```

2. **切换到游戏分支**
   ```bash
   git checkout claude/mario-style-game-011CUKUhoG7o94TAu5b17WyM
   ```

3. **安装依赖**
   ```bash
   npm i -g pnpm  # 如果还没安装pnpm
   pnpm install
   ```

4. **创建环境变量文件（可选，游戏不需要API密钥）**
   ```bash
   cp .env.example .env
   ```
   注意：马里奥游戏不需要GEMINI_API_KEY，可以留空

5. **启动开发服务器**
   ```bash
   pnpm run dev
   ```

6. **访问游戏**

   打开浏览器访问：`http://localhost:3000/mario`

### 方法2：通过Vercel部署（推荐）

1. **Fork这个仓库到你的GitHub账号**

2. **访问 [Vercel](https://vercel.com)**

3. **导入你的项目**
   - 点击 "New Project"
   - 选择你fork的仓库
   - 选择分支：`claude/mario-style-game-011CUKUhoG7o94TAu5b17WyM`

4. **配置环境变量（可选）**
   - GEMINI_API_KEY 可以留空（游戏不需要）

5. **部署**
   - 点击 "Deploy"
   - 等待部署完成

6. **访问游戏**

   部署完成后访问：`https://你的域名.vercel.app/mario`

### 方法3：通过Netlify部署

1. **Fork这个仓库到你的GitHub账号**

2. **访问 [Netlify](https://netlify.com)**

3. **导入你的项目**
   - 点击 "Add new site" → "Import an existing project"
   - 选择你fork的仓库
   - 选择分支：`claude/mario-style-game-011CUKUhoG7o94TAu5b17WyM`

4. **配置构建设置**
   - Build command: `pnpm run build:netlify`
   - Publish directory: `dist`

5. **部署并访问**

   部署完成后访问：`https://你的站点.netlify.app/mario`

### 方法4：构建静态文件

如果你想要构建静态HTML文件以便在任何Web服务器上托管：

```bash
# 构建项目
pnpm run build

# 预览构建结果
pnpm run preview
```

构建后的文件会在 `dist` 目录中，可以将其部署到任何静态文件托管服务。

## 常见问题

**Q: 游戏卡顿怎么办？**
A: 尝试关闭浏览器的其他标签页，或使用Chrome/Edge等现代浏览器。

**Q: 键盘控制没反应？**
A: 确保点击了游戏画布区域，让页面获得焦点。

**Q: 可以在手机上玩吗？**
A: 目前游戏只支持键盘操作，手机触摸控制暂未实现。

**Q: 如何修改游戏？**
A: 游戏代码在 `src/pages/mario.astro` 文件中，你可以修改关卡设计、敌人数量等参数。

## 技术细节

- **框架**: Astro + HTML5 Canvas
- **渲染**: Canvas 2D API
- **物理引擎**: 自定义重力和碰撞检测系统
- **游戏循环**: requestAnimationFrame (60 FPS)

## 开发路线图

未来可能添加的功能：
- [ ] 更多关卡
- [ ] 道具系统（蘑菇、火焰花等）
- [ ] 音效和背景音乐
- [ ] 移动端触摸控制
- [ ] 本地排行榜
- [ ] 更多敌人类型

## 贡献

欢迎提交问题和改进建议！

## 许可证

与主项目保持一致
