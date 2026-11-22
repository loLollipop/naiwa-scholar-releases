# Naiwa Scholar

Naiwa Scholar 是面向论文整理、PDF 阅读和双语阅读的 Windows 桌面科研工具，目前免费开放体验，欢迎反馈问题和建议。

## 下载

- [下载 Windows x64 安装包](https://github.com/loLollipop/naiwa-scholar-releases/releases/latest/download/Naiwa-Scholar-Windows-x64-Setup.exe)
- [版本与更新说明](https://github.com/loLollipop/naiwa-scholar-releases/releases)
- [SHA-256 校验值](https://github.com/loLollipop/naiwa-scholar-releases/releases/latest/download/SHA256SUMS.txt)

当前提供 Windows x64 安装包。阅读模型、英文 OCR、PDFium、离线词典与 Agent 适配器随包提供。在线翻译和 AI 功能需要网络及用户自己的相应服务配置，免费提供软件不代表附赠第三方 API 额度。

安装包尚未使用 Windows Authenticode 证书签名，Windows 可能显示未知发布者或安全提示。缺少 WebView2 时，安装过程需要联网下载运行时。仅在确认下载来源后安装。

## 安装与更新

运行安装程序并按向导选择安装目录。安装完成后打开 Naiwa Scholar，按照首次启动向导选择文库位置。

新版通过本仓库手动下载更新，升级时选择原安装目录。配置保存在安装目录的 `userdata` 中；论文和笔记保存在自己选择的文库中。更新前建议备份重要文库，不要手动删除 `userdata`。

## 反馈

[提交问题或建议](https://github.com/loLollipop/naiwa-scholar-releases/issues/new/choose)。请说明软件版本、Windows 版本、操作步骤、实际结果和预期结果；可以附必要截图。不要上传 API Key、账号凭据或不便公开的论文和个人资料。

本仓库仅维护公开安装包、版本说明和用户反馈，不包含应用源码。

## 上游与许可

Naiwa Scholar 基于 [poco-ai/Agentero](https://github.com/poco-ai/Agentero) 维护。上游 MIT 版权和许可随安装包保留；第三方声明随包置于 `licenses` 目录。仓库的 MIT 许可不授予第三方名称、商标或角色美术素材的使用权。
