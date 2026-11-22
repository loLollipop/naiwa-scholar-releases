# Naiwa Scholar

Naiwa Scholar 是面向论文整理、PDF 阅读和双语阅读的 Windows 桌面科研工具，目前免费开放体验，欢迎反馈问题和建议。

## 下载

- [下载 Windows x64 安装包](https://github.com/loLollipop/naiwa-scholar-releases/releases/latest/download/Naiwa-Scholar-Windows-x64-Setup.exe)
- [版本与更新说明](https://github.com/loLollipop/naiwa-scholar-releases/releases)
- [SHA-256 校验值](https://github.com/loLollipop/naiwa-scholar-releases/releases/latest/download/SHA256SUMS.txt)
- [0.16.2 完整对应源码](https://github.com/loLollipop/naiwa-scholar-releases/releases/download/v0.16.2/Naiwa-Scholar-0.16.2-Source.zip)

当前提供 Windows x64 安装包。阅读模型、英文 OCR、PDFium、离线词典与 Agent 适配器随包提供。在线翻译和 AI 功能需要网络及用户自己的相应服务配置，免费提供软件不代表附赠第三方 API 额度。

安装包尚未使用 Windows Authenticode 证书签名，Windows 可能显示未知发布者或安全提示。缺少 WebView2 时，安装过程需要联网下载运行时。仅在确认下载来源后安装。

## 安装与更新

运行安装程序并按向导选择安装目录。安装完成后打开 Naiwa Scholar，按照首次启动向导选择文库位置。

新版通过本仓库手动下载更新，升级时选择原安装目录。配置保存在安装目录的 `userdata` 中；论文和笔记保存在自己选择的文库中。更新前建议备份重要文库，不要手动删除 `userdata`。

## 反馈

[提交问题或建议](https://github.com/loLollipop/naiwa-scholar-releases/issues/new/choose)。请说明软件版本、Windows 版本、操作步骤、实际结果和预期结果；可以附必要截图。不要上传 API Key、账号凭据或不便公开的论文和个人资料。

每版 Release 同时提供安装包、完整对应源码和 SHA-256 校验值。源码包内的 `BUILDING.md` 说明 Windows 构建方法，`SOURCE-FILES.sha256` 标识本版源文件；产品模板、构建脚本、本地依赖补丁和 LaTeX 组件的完整上游源码均包含在内。开发仓库及其提交历史继续独立维护。

## 从源码构建

解压对应版本的源码包，在已安装 Rust MSVC、Windows SDK、CMake、LLVM/libclang、Node.js、pnpm 和 VC++ 可再发行组件的 Windows x64 开发终端中运行：

```powershell
pnpm install --frozen-lockfile
pnpm desktop:build
```

安装包生成到 `target/release/bundle/nsis/`。构建无需维护者的本机配置或 API Key；外部依赖和阅读资源由锁文件及暂存脚本下载。具体工具链版本和步骤以源码包内的 `BUILDING.md` 为准。

## 上游与许可

Naiwa Scholar 基于 [poco-ai/Agentero](https://github.com/poco-ai/Agentero) 维护。此版本包含 AGPL-3.0-or-later 的 `codemirror-lang-latex 0.6.1`，组合应用按 [GNU AGPL v3 或更新版本](COPYING) 分发。完整对应源码与安装包在同版 Release 中免费提供。

原有组件的版权与许可继续保留；本仓库的 `LICENSE` 保留上游 MIT 声明，不代表组合应用只受 MIT 许可约束。第三方声明随安装包置于 `licenses` 目录，详细分发说明见 `licenses/third-party/Naiwa-Scholar-DISTRIBUTION.txt`。代码许可不授予第三方名称、商标或角色美术素材的使用权。
