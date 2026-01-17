# PPTist 修改版本说明

## 原始项目信息

- **项目名称**: PPTist
- **原始作者**: [pipipi-pikachu](https://github.com/pipipi-pikachu)
- **原始仓库**: https://github.com/pipipi-pikachu/PPTist
- **许可证**: GNU Affero General Public License v3.0 (AGPL-3.0)

## 修改说明

本仓库是基于 [PPTist](https://github.com/pipipi-pikachu/PPTist) 项目的修改版本，主要用于整合到 AI 教案生成系统中。

### 主要修改内容

1. **API 集成修改**
   - 修改了 `src/services/index.ts` 中的 API 端点配置
   - 将 PPT 生成相关的 API 从原始端点改为指向项目后端服务器
   - 后端服务器地址: `http://localhost:5001` (开发环境)

2. **AI 模型更换**
   - 将原始的 GLM 和 Doubao 模型更换为通义千问 (Qwen) 模型
   - 修改的文件:
     - `src/views/Editor/AIPPTDialog.vue`: AI PPT 生成模型选择
     - `src/services/index.ts`: AI 写作功能模型配置

3. **功能移除**
   - 移除了在线图库功能
   - 修改的文件: `src/views/Editor/CanvasTool/index.vue`

4. **UI 调整**
   - 优化了按钮布局和对齐方式
   - 添加了 group-btn 类以保持界面一致性

### 修改的文件列表

- `src/services/index.ts` - API 端点配置和 AI 模型设置
- `src/views/Editor/AIPPTDialog.vue` - AI PPT 对话框和模型选择
- `src/views/Editor/CanvasTool/index.vue` - 画布工具栏（移除在线图库）

## 许可证声明

本修改版本继续遵循 **GNU Affero General Public License v3.0 (AGPL-3.0)** 协议。

### AGPL-3.0 协议要点

1. **开源义务**:
   - 任何基于此代码的修改版本都必须完整开源
   - 必须保持 AGPL-3.0 协议，不得更换为其他协议

2. **网络服务也要开源**:
   - 即使只是通过网络提供服务，也必须遵守开源义务
   - 用户通过网络访问时，必须能够获取到源代码

3. **保留版权声明**:
   - 不得删除原始作者的版权信息和许可证声明
   - 必须明确标注代码来源

4. **不能加额外限制**:
   - 不能在衍生代码上添加限制性条款
   - 不能要求付费才能使用代码

### 详细协议内容

请查看项目根目录下的 [LICENSE](./LICENSE) 文件，或访问官方文档：
https://www.gnu.org/licenses/agpl-3.0.html

## 使用说明

### 安装依赖

```bash
npm install
```

### 开发模式运行

```bash
npm run dev
```

浏览器访问: http://127.0.0.1:5173/

### 构建生产版本

```bash
npm run build
```

## 免责声明

- 本修改版本仅用于学习和研究目的
- 原始作者和修改者不对使用后果负责
- 软件按"原样"提供，不提供任何明示或暗示的保证

## 联系方式

如有关于此修改版本的问题，请在 GitHub 仓库中提出 Issue。

---

**重要提醒**: 如果您计划将此项目用于商业用途，请务必仔细阅读并遵守 AGPL-3.0 协议的所有条款。原始作者提供了独立的商业授权选项，详情请参阅原始项目的 README 文件。
