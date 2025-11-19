# Open Weather13 MCP Server

English | [简体中文](./README.md) | [繁體中文](./README_ZH-TW.md)

## 🚀 Quick Start with EMCP Platform

**[EMCP](https://sit-emcp.kaleido.guru)** is a powerful MCP server management platform that allows you to quickly use various MCP servers without manual configuration!

### Quick Start:

1. 🌐 Visit **[EMCP Platform](https://sit-emcp.kaleido.guru)**
2. 📝 Register and login
3. 🎯 Go to **MCP Marketplace** to browse all available MCP servers
4. 🔍 Search or find this server (`bach-open_weather13`)
5. 🎉 Click the **"Install MCP"** button
6. ✅ Done! You can now use it in your applications

### EMCP Platform Advantages:

- ✨ **Zero Configuration**: No need to manually edit config files
- 🎨 **Visual Management**: Easy-to-use GUI for managing all MCP servers
- 🔐 **Secure & Reliable**: Centralized API key and authentication management
- 🚀 **One-Click Install**: Rich selection of servers in MCP Marketplace
- 📊 **Usage Statistics**: Real-time service call monitoring

Visit **[EMCP Platform](https://sit-emcp.kaleido.guru)** now to start your MCP journey!


---

## Introduction

This is an automatically generated MCP server using [FastMCP](https://fastmcp.wiki) for accessing the Open Weather13 API.

- **PyPI Package**: `bach-open_weather13`
- **Version**: 1.0.0
- **Transport Protocol**: stdio


## 安装

### 从 PyPI 安装:

```bash
pip install bach-open_weather13
```

### 从源码安装:

```bash
pip install -e .
```

## 运行

### 方式 1: 使用 uvx（推荐，无需安装）

```bash
# 运行（uvx 会自动安装并运行）
uvx --from bach-open_weather13 bach_open_weather13

# 或指定版本
uvx --from bach-open_weather13@latest bach_open_weather13
```

### 方式 2: 直接运行（开发模式）

```bash
python server.py
```

### 方式 3: 安装后作为命令运行

```bash
# 安装
pip install bach-open_weather13

# 运行（命令名使用下划线）
bach_open_weather13
```

## Configuration

### API Authentication

This API requires authentication. Please set environment variable:

```bash
export API_KEY="your_api_key_here"
```

### Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `API_KEY` | API Key | Yes |
| `PORT` | N/A | No |
| `HOST` | N/A | No |



### 在 Claude Desktop 中使用

编辑 Claude Desktop 配置文件 `claude_desktop_config.json`:


```json
{
  "mcpServers": {
    "open_weather13": {
      "command": "python",
      "args": ["E:\path\to\open_weather13\server.py"],
      "env": {
        "API_KEY": "your_api_key_here"
      }
    }
  }
}
```

**Note**: Replace `E:\path\to\open_weather13\server.py` with the actual server file path.


## 可用工具

此服务器提供以下工具:


### `v2___3_hour_forecast_5_days`

Get 5 days weather forecast data by Latitude \u0026 Longitude

**端点**: `GET /fivedaysforcast`


**参数**:

- `latitude` (string) *必需*: Example value: 40.730610

- `longitude` (string) *必需*: Example value: -73.935242

- `lang` (string): We support the following languages that you can use with the corresponded lang values: AFAfrikaans, ALAlbanian, ARArabic, AZAzerbaijani, BGBulgarian, CACatalan, CZCzech, DADanish, DEGerman, ELGreek, ENEnglish, EUBasque, FAPersian (Farsi), FIFinnish, FRFrench, GLGalician, HEHebrew, HIHindi, HRCroatian, HUHungarian, IDIndonesian, ITItalian, JAJapanese, KRKorean, LALatvian, LTLithuanian, MKMacedonian, NONorwegian, NLDutch, PLPolish, PTPortuguese, PT_BRPortuguês Brasil, RORomanian, RURussian, SESwed

- `latitude` (string) *必需*: Example value: 40.730610

- `longitude` (string) *必需*: Example value: -73.935242

- `lang` (string): Example value: EN



---


### `v2___current_weatherby_latitude_u0026_longitude`

Get Current Weather Data by Latitude \u0026 Longitude [Documentation](https://rapidapi.com/worldapi/api/open-weather13/details)

**端点**: `GET /latlon`


**参数**:

- `latitude` (string) *必需*: Example value: 40.730610

- `longitude` (string) *必需*: Example value: -73.935242

- `lang` (string): We support the following languages that you can use with the corresponded lang values: AFAfrikaans, ALAlbanian, ARArabic, AZAzerbaijani, BGBulgarian, CACatalan, CZCzech, DADanish, DEGerman, ELGreek, ENEnglish, EUBasque, FAPersian (Farsi), FIFinnish, FRFrench, GLGalician, HEHebrew, HIHindi, HRCroatian, HUHungarian, IDIndonesian, ITItalian, JAJapanese, KRKorean, LALatvian, LTLithuanian, MKMacedonian, NONorwegian, NLDutch, PLPolish, PTPortuguese, PT_BRPortuguês Brasil, RORomanian, RURussian, SESwed

- `latitude` (string) *必需*: Example value: 40.730610

- `longitude` (string) *必需*: Example value: -73.935242

- `lang` (string): Example value: EN



---


### `v2___current_weather_by_city_name`

Get Current Weather Data by City Name [Documentation](https://rapidapi.com/worldapi/api/open-weather13/details)

**端点**: `GET /city`


**参数**:

- `city` (string) *必需*: Example value: new york

- `lang` (string): We support the following languages that you can use with the corresponded lang values: AFAfrikaans, ALAlbanian, ARArabic, AZAzerbaijani, BGBulgarian, CACatalan, CZCzech, DADanish, DEGerman, ELGreek, ENEnglish, EUBasque, FAPersian (Farsi), FIFinnish, FRFrench, GLGalician, HEHebrew, HIHindi, HRCroatian, HUHungarian, IDIndonesian, ITItalian, JAJapanese, KRKorean, LALatvian, LTLithuanian, MKMacedonian, NONorwegian, NLDutch, PLPolish, PTPortuguese, PT_BRPortuguês Brasil, RORomanian, RURussian, SESwed

- `city` (string) *必需*: Example value: new york

- `lang` (string): Example value: EN



---



## 技术栈

- **FastMCP**: 快速、Pythonic 的 MCP 服务器框架
- **传输协议**: stdio
- **HTTP 客户端**: httpx

## 开发

This server is automatically generated by [API-to-MCP](https://github.com/BACH-AI-Tools/api-to-mcp) tool.

Version: 1.0.0
