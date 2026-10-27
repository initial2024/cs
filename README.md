# DeepSeek Web Gateway V2 验收官

这是一个独立、只读的 DSH Agent preset，用于检查本次 Gateway V2 APK、provider 插件与发布包。

安装本地 tgz/zip 后，新建会话并选择 **「DeepSeek Web Gateway V2 验收官」**。把发布包或解压目录路径交给它，例如：

```text
只读验收 /sdcard/Download/DSH-Web-Gateway-V2-release.zip。先做静态验收；未经我允许不要安装 APK。
```

它被要求严格区分 `PASS_STATIC` 与真机 `PASS`，不会把“代码里有功能”冒充“手机上已经实测通过”。
