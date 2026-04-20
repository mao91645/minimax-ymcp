# MiniMax-YMCP

A Model Context Protocol (MCP) server that provides 11 tools powered by MiniMax APIs, including speech synthesis, video generation, image generation, music generation, web search, and image understanding.

## Features

- 🗣️ **Text-to-Speech** — Convert text to speech with emotions and voice cloning
- 🎬 **Video Generation** — Text-to-video and image-to-video (I2V)
- 🎨 **Image Generation** — Text-to-image with multiple aspect ratios
- 🎵 **Music Generation** — Generate music from lyrics and prompts
- 🔍 **Web Search** — Real-time web search with MiniMax
- 🖼️ **Image Understanding** — Analyze and describe images with AI vision
- 💬 **Text Chat** — Chat with MiniMax large language models
- 📋 **Prompt Management** — Save and reuse system prompts
- 📚 **Resource Browser** — Browse available API resources

## Available Tools

| Tool | Description |
|------|-------------|
| `text_to_audio` | Text-to-speech with emotion control |
| `text_to_image` | Generate images from text prompts |
| `video_generation` | Generate videos from text or images |
| `music_generation` | Create music with lyrics and style |
| `web_search` | Real-time web search |
| `understand_image` | Analyze images with AI vision |
| `chat` | Chat with MiniMax LLM |
| `voice_clone` | Clone voice from audio samples |
| `voice_design` | Design custom voices |
| `list_prompts` | List saved system prompts |
| `list_voices` | List available voice options |

## Installation

### Quick Start (uvx)

```bash
uvx --from github.com/mao91645/minimax-ymcp minimax-ymcp
```

### Claude Desktop (Config File)

**macOS/Linux:** `~/.config/claude/claude_desktop_config.json`

**Windows:** `%APPDATA%\Claude\claude_desktop_config.json`

```json
{
  "mcpServers": {
    "minimax-ymcp": {
      "command": "uvx",
      "args": ["--from", "github.com/mao91645/minimax-ymcp", "minimax-ymcp"]
    }
  }
}
```

### Cursor

1. Open Cursor Settings → MCP
2. Click "Add new MCP server"
3. Enter the command:

```
uvx --from github.com/mao91645/minimax-ymcp minimax-ymcp
```

### Windsurf

1. Open Windsurf Settings → MCP
2. Add new server:

```yaml
mcp-ymcp:
  command: uvx
  args: ["--from", "github.com/mao91645/minimax-ymcp", "minimax-ymcp"]
```

### Trae

```json
{
  "mcpServers": {
    "minimax-ymcp": {
      "command": "uvx",
      "args": ["--from", "github.com/mao91645/minimax-ymcp", "minimax-ymcp"]
    }
  }
}
```

### OpenClaw (Windows)

Configure in OpenClaw's MCP server settings:

```
Name: minimax-ymcp
Command: uvx --from github.com/mao91645/minimax-ymcp minimax-ymcp
```

### Claude Code / Hermes Agent

```bash
claude --mcp-Ymcp "uvx --from github.com/mao91645/minimax-ymcp minimax-ymcp"
```

### Docker

```bash
docker pull ghcr.io/mao91645/minimax-ymcp:latest
```

## Configuration

The following environment variables are supported:

| Variable | Default | Description |
|----------|---------|-------------|
| `MINIMAX_API_KEY` | Required | Your MiniMax API key |
| `MINIMAX_GROUP_ID` | Required | Your MiniMax Group ID |
| `MINIMAX_API_HOST` | `https://api.minimaxi.com` | API endpoint |
| `DEFAULT_VOICE_ID` | `female-shaonv` | Default voice for TTS |
| `DEFAULT_MUSIC_MODEL` | `music-2.6` | Music generation model |
| `DEFAULT_VIDEO_MODEL` | `MiniMax-Hailuo-02` | Video generation model |
| `DEFAULT_IMAGE_MODEL` | `image-01` | Image generation model |

## Environment Setup

Create a `.env` file in your project:

```bash
MINIMAX_API_KEY=your_api_key_here
MINIMAX_GROUP_ID=your_group_id_here
```

## Common Issues

### Q: `uvx` command not found

Install `uv` first:

```bash
# macOS/Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# Windows (PowerShell)
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

### Q: API key error

Make sure `MINIMAX_API_KEY` and `MINIMAX_GROUP_ID` are set correctly in your environment.

### Q: Video/Image generation fails

Check that your account has sufficient quota for the respective service.

## License

MIT License

## Links

- [GitHub Repository](https://github.com/mao91645/minimax-ymcp)
- [MiniMax API Docs](https://www.minimaxi.com/document)
