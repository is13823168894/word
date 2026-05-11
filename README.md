# Word Hello World 插件

一个简单的 Word Add-in 示例，用于演示如何在 Word 中创建加载项。

## 功能

- **插入文本**: 点击按钮在文档中插入 "Hello World! 你好世界！"
- **获取选中文本**: 获取当前选中的文本
- **统计字数**: 统计文档总字数

## 安装步骤

### 方法一：从 GitHub 加载（推荐）

1. 开启 GitHub Pages：
   - 进入仓库 **Settings** → **Pages**
   - Source 选择 **Deploy from a branch**
   - Branch 选择 **main**，文件夹选 **/ (root)**
   - 点击 **Save**

2. 等待部署完成（约1分钟），访问地址：
   ```
   https://is13823168894.github.io/word/taskpane.html
   ```

3. 在 Word 中加载：
   - 打开 Word → **插入** → **获取加载项**
   - 选择 **管理我的加载项** → **上载我的加载项**
   - 选择本仓库中的 `manifest.xml` 文件

### 方法二：本地加载

1. 下载 `manifest.xml` 和 `taskpane.html` 文件
2. 启动 HTTPS 服务器：
   ```bash
   npx http-server -p 8080 -S -C <证书路径> -K <密钥路径> --cors
   ```
3. 在 Word 中通过文件路径加载 manifest.xml

## 文件说明

| 文件 | 说明 |
|------|------|
| `manifest.xml` | 加载项清单配置 |
| `taskpane.html` | 主界面（包含所有代码）|
| `README.md` | 说明文档 |

## 技术要点

- 使用 Office.js 与 Word 交互
- 所有代码内联在 taskpane.html 中
- 需要 HTTPS 环境运行

## 参考资料

- [Office Add-ins Documentation](https://docs.microsoft.com/office/dev/add-ins/)
- [Office.js API Reference](https://docs.microsoft.com/office/dev/add-ins/reference/overview/word-add-ins-reference-overview)
