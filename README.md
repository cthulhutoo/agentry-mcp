# Agentry MCP Server

**AI Agent Registry & Discovery** — search, register, and evaluate AI agents via the Model Context Protocol.

[![MCP](https://img.shields.io/badge/MCP-SSE-blue)](https://api.agentry.com/mcp)
[![Agents](https://img.shields.io/badge/Agents-122+-green)](https://agentry.com/agents)
[![A2A](https://img.shields.io/badge/A2A-Compatible-orange)](https://api.agentry.com/.well-known/agent.json)

## Overview

Agentry is a live AI agent directory with 122+ agents across 11 categories. The MCP server exposes the full directory as tools — search, register, evaluate, and transact with AI agents programmatically.

**No authentication required** for read endpoints.

## Quick Start

### SSE Connection

```
https://api.agentry.com/mcp
```

### Claude Desktop / Cursor

Add to your MCP config:

```json
{
  "mcpServers": {
    "agentry": {
      "transport": "sse",
      "url": "https://api.agentry.com/mcp"
    }
  }
}
```

## Available Tools

| Tool | Description |
|------|-------------|
| `search_agents` | Search the directory by keyword, category, or capability |
| `get_agent_details` | Full agent details — trust scores, pricing, integrations |
| `register_agent` | Submit a new AI agent for listing |
| `a2a_discovery` | Google A2A protocol compatible agent discovery |
| `ecash_payments` | Cashu ecash payment rails for agent-to-agent transactions |

## Discovery Endpoints

| Endpoint | URL |
|----------|-----|
| MCP SSE | `https://api.agentry.com/mcp` |
| MCP Metadata | `https://api.agentry.com/.well-known/mcp` |
| A2A Agent Card | `https://api.agentry.com/.well-known/agent.json` |
| agents.json | `https://api.agentry.com/.well-known/agents.json` |
| OpenAPI Docs | `https://api.agentry.com/docs` |
| Website | [agentry.com](https://agentry.com) |

## Features

- **122+ AI agents** across 11 categories (Sales, Support, Dev Tools, Marketing, etc.)
- **Trust scoring** — automated verification and trust tier ranking
- **A2A Protocol** — Google Agent-to-Agent compatible discovery
- **Ecash payments** — Cashu token support for agent-to-agent transactions via Lightning Network
- **No auth required** — public read access to the full directory
- **Real-time SSE** — streaming MCP transport

## Examples

### Search for agents
```
Use the search_agents tool to find "customer support agents with Slack integration"
```

### Get agent details
```
Use get_agent_details with agent_id "agent-0001" to see full trust score and capabilities
```

### Register a new agent
```
Use register_agent with name, url, and description to list your agent in the directory
```

## API

Full REST API documentation: [api.agentry.com/docs](https://api.agentry.com/docs)

## License

MIT
