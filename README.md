# ComfyUI Agent Bridge — ComfyUI extension

This is the ComfyUI-side extension of [ComfyUI Agent Bridge](https://github.com/sfysyyds/ComfyUI-Agent-Bridge). It exposes the currently open canvas to a local MCP client. It adds no generation nodes; the browser extension and local bridge routes are the product.

**Installing this package from ComfyUI-Manager does not install the MCP server or Skill.** For AI control, download the [matching v1.3.3 release](https://github.com/sfysyyds/ComfyUI-Agent-Bridge/releases/tag/v1.3.3), extract it, and run from the extracted folder:

```powershell
powershell -ExecutionPolicy Bypass -File ".\comfyui-agent\scripts\install.ps1" -ComfyUIRoot "C:\your\ComfyUI" -SkipPlugin
```

Restart both ComfyUI and your AI client, then run `comfyui-agent\scripts\diagnose.ps1` from the same folder. Do not install a second copy of the ComfyUI plugin with the full installer.

The bridge listens on the local ComfyUI server and has no internet-facing authentication. Do not expose its control port to the public internet. The bridge does not save workflows; ComfyUI's own auto-save settings still apply.

中文说明、MCP/Skill 安装及完整源码：[主仓库](https://github.com/sfysyyds/ComfyUI-Agent-Bridge)。
