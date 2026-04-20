# MiniMax-YMCP

📄 [中文说明书](./中文说明书.md)

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

### Claude Desktop

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

```
uvx --from github.com/mao91645/minimax-ymcp minimax-ymcp
```

### Windsurf

```yaml
mcp-ymcp:
  command: uvx
  args: ["--from", "github.com/mao91645/minimax-ymcp", "minimax-ymcp"]
```

### Docker

```bash
docker pull ghcr.io/mao91645/minimax-ymcp:latest
```

## Configuration

| Variable | Default | Description |
|----------|---------|-------------|
| `MINIMAX_API_KEY` | Required | Your MiniMax API key |
| `MINIMAX_GROUP_ID` | Required | Your MiniMax Group ID |
| `MINIMAX_API_HOST` | `https://api.minimaxi.com` | API endpoint |

## License

MIT License

## Links

- [GitHub Repository](https://github.com/mao91645/minimax-ymcp)
- [MiniMax API Docs](https://www.minimaxi.com/document)
