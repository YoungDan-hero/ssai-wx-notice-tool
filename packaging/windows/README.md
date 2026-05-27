# Windows 打包说明

本项目的 Windows 版使用 PyInstaller 打包，输出为免安装目录。

## 打包环境

- Windows 10/11
- Python 3.11 或更新版本
- 已安装并登录 Windows 微信客户端

## 打包命令

在项目根目录运行：

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
packaging\windows\build_windows.ps1
```

打包结果输出到：

```text
dist\SSAI-WX-Notice-Tool\
```

可执行文件为：

```text
dist\SSAI-WX-Notice-Tool\SSAI-WX-Notice-Tool.exe
```

## 使用说明

1. 打开并登录 Windows 微信客户端。
2. 将要通知的群聊拆分成独立聊天窗口。
3. 启动 `SSAI-WX-Notice-Tool.exe`。
4. 点击“刷新窗口”，确认右侧列表只包含本次要发送的窗口。
5. 输入文字或添加图片、文档后点击“同步发送”。

Windows 版会枚举当前可见的微信独立窗口，通过系统剪贴板粘贴内容，并模拟 `Ctrl+V` 和回车发送。
