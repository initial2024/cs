# DeepSeek Web Gateway V2 验收官

这是一个独立、只读的 DSH Agent preset，用于检查本次 Gateway V2 APK、provider 插件与发布包。

安装本地 tgz/zip 后，新建会话并选择 **「DeepSeek Web Gateway V2 验收官」**。把发布包或解压目录路径交给它，例如：

```text
只读验收 /sdcard/Download/DSH-Web-Gateway-V2-release.zip。先做静态验收；未经我允许不要安装 APK。
```

它被要求严格区分 `PASS_STATIC` 与真机 `PASS`，不会把“代码里有功能”冒充“手机上已经实测通过”。


## v1.1.0 — original core + updated DSH

新增验收重点：

- 原 AI Gateway 核心冻结，不以新 WebView/DOM 逻辑重写原输入、发送、上传、登录与悬浮窗；
- DSH `wet` 0.4.0 优先连接 1601，必要时自动回退 8787；
- DeepSeek / ChatGPT / Grok / GLM 四个原模型 id 均可见；
- 普通 `client_disconnected` 或 UI/连接短暂变化不得立即截停正在生成的网页回答；
- 只有明确用户取消才允许即时停止；
- 自动 fresh-chat 只允许由明确的 provider context/conversation-limit 证据触发。
