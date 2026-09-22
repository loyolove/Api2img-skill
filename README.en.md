# Api2img Skill (Tutorial for Manual API Endpoint & API Key Setup)

[中文](README.md) | [English](README.en.md)

## Features

**`Allow any Agent using non-official API keys to achieve near-native image generation capability.`**

api2img is designed for users who use Agents via relay APIs and require image generation & image editing features.
It supports skill-installable Agents including `Codex`, `Claude Code`, `OpenClaw`, `Hermes`, and works with other manually integrable Agents.

![api2img illustration](assets/readme-cn-cover.jpg)

## Installation

Copy the link below and send it to your Agent:
[https://github.com/loyolove/api2img-skill/](https://github.com/loyolove/api2img-skill/)

Install api2img as a global skill.

## Recommended Image Generation API Relay Providers

[](https://a6api.com/?auth=register&aff=OqhO)[https://a6api.com](https://a6api.com)
⭐️ Aggregated API relay hub integrating multiple vendors at competitive prices. The Image2 model starts at 0.01~0.2 CNY per image. Built-in routing supports multiple fallback API endpoints.

- Also provides Claude Code, DeepSeek, Qwen and various LLM models at budget-friendly rates.

---

[](https://apinebula.com/8Rvk7M)[https://apinebula.com](https://apinebula.com)
Established and reliable platform built for stability! Great alternative for users tired of personal relay services with frequent image generation failures.

- Long-running stable service operated by a registered company; invoices available.
- Image2 image generation (0.05 CNY per image).
- Supports Claude Code / Codex (GPT models at 48% off).

---

## Invocation

The Agent will automatically invoke this skill when needed. You can also trigger it manually for regular image tasks:

- 【Generate】Generate an image of xxx
- 【Edit】Replace a specific part of the image
- 【Upload】Edit xxx within the image I uploaded

## Supported Commands

Use natural language to instruct your Agent:

```
# Installation
- Install api2img as a global skill (default)
- Install api2img to the current project

# Configuration
- Help me set the api2img base url
- Help me update the api2img api key
- Help me clear api2img configurations
```

## Appendix 1. Manually Create Config Files (Optional)

If `npx` does not work in your current PowerShell session, manually create the config folder and files.

### 1. Create the Directory

Paste this path into File Explorer address bar:

```
%USERPROFILE%\.api2img
```

Create the folder if missing:

```
C:\Users\<your username>\.api2img
```

### 2. Create `config.json`

Inside the `.api2img` folder, create `config.json`:

```
{
  "baseUrl": "https://your-api-endpoint-url"
}
```

### 3. Create `secret.json`

On Windows, api2img stores your API key locally in a file. Create `secret.json` in the same directory:

```
{
  "apiKey": "YOUR_API_KEY"
}
```

Replace `YOUR_API_KEY` with your actual key. **Never commit this file to Git.**

### Folder Structure after Manual Setup

```
C:\Users\<your username>\.api2img\
├── config.json
└── secret.json
```

> 
> Note: Ensure your filenames are not `config.json.txt` or `secret.json.txt`. Turn on **View → Show → File name extensions** in File Explorer.

## Appendix 2. Generate Images Directly in Codex

Once configured, no manual commands are required each time. Simply describe your image requirements inside Codex, for example:

> 
> Generate a realistic commercial ad photo of indoor plants, warm natural light, minimalist home background, landscape orientation, resolution 1536×1024.

Codex will invoke your configured image API via the installed `api2img` skill.

## Privacy Statement

- This skill does not upload any of your data.
- When generating images, your prompts and uploaded images are sent to the third-party API relay provider you configured. Do not process ID documents, facial photos, business confidential materials or other sensitive private data.
