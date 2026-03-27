# go-input-monitor

中文 | [English](README.md)

一款使用 Go 编写的轻量级 Windows 输入监控工具，适用于安全研究与渗透测试。

## 功能

- **键盘记录** - 通过 `SetWindowsHookEx` 低级键盘钩子捕获按键，支持 Shift/CapsLock 状态识别
- **窗口标题追踪** - 实时记录当前前台窗口标题
- **剪贴板监控** - 检测并记录剪贴板内容变化

## 构建

```bash
go build -ldflags="-s -w -H windowsgui" -o go-input-monitor.exe
```

> `-H windowsgui` 参数用于隐藏运行时的控制台窗口。

## 使用

在 Windows 系统上运行编译后的可执行文件，捕获的数据将保存到可执行文件同目录下的 `Mcafee_dump.tmp` 文件中。

## 技术栈

- Go 1.24+
- Windows API (`user32.dll`)
- [w32](https://github.com/TheTitanrain/w32) - Windows API 绑定
- [clipboard](https://github.com/atotto/clipboard) - 跨平台剪贴板访问

## 免责声明

本工具**仅供授权的安全测试、教育目的和研究使用**。未经他人同意擅自使用本工具进行监控属于违法行为，作者不对任何滥用行为承担责任。

## 许可证

MIT
