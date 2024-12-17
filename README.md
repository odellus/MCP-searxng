# MCP-searxng

An MCP server for connecting agentic systems to search systems via searXNG.

<a href="https://glama.ai/mcp/servers/sl2zl8vaz8"><img width="380" height="200" src="https://glama.ai/mcp/servers/sl2zl8vaz8/badge" /></a>

## Tools

Search the web with searXNG

## Prompts

```python
search(query: str) -> f"Searching for {query} using searXNG"
```

## Usage

1) Add the server to claude desktop (the entrypoint is main.py)

Clone the repo and add this json to claude desktop

```json
{
  "mcpServers": {
    "searxng": {
      "command": "uv", 
      "args": [
        "--project",
        "/absoloute/path/to/MCP-searxng/",
        "run",
        "/absoloute/path/to/MCP-searxng/mcp-searxng/main.py"
      ]
    }
  }
}
```

obviously you will need to change the paths to match your environment

2) set the environment variable `SEARXNG_URL` to the url of the searxng server (default is `http://localhost:8080`)

3) run your MCP client and you should be able to search the web with searxng

Note: if you are using claude desktop make sure to kill the process (task manager or equivalent) before running the server again
