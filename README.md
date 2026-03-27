# go-input-monitor

A lightweight Windows input monitoring tool written in Go, designed for security research and penetration testing.

## Features

- **Keystroke Capture** - Low-level keyboard hook via `SetWindowsHookEx`, supports Shift/CapsLock state detection
- **Window Title Tracking** - Real-time logging of the foreground window title
- **Clipboard Monitoring** - Detects and records clipboard content changes

## Build

```bash
go build -ldflags="-s -w -H windowsgui" -o go-input-monitor.exe
```

> The `-H windowsgui` flag hides the console window at runtime.

## Usage

Run the compiled executable on a Windows system. Captured data is saved to `Mcafee_dump.tmp` in the same directory as the executable.

## Tech Stack

- Go 1.24+
- Windows API (`user32.dll`)
- [w32](https://github.com/TheTitanrain/w32) - Windows API bindings
- [clipboard](https://github.com/atotto/clipboard) - Cross-platform clipboard access

## Disclaimer

This tool is intended **solely for authorized security testing, educational purposes, and research**. Unauthorized use of this tool to monitor others without consent is illegal. The author assumes no liability for misuse.

## License

MIT
