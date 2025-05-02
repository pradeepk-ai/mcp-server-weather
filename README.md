### MCP Server that invokes Weather API
- Weather API used - Mateo - https://api.open-meteo.com/v1/
- Server.py - Python code to define MCP tool and invoke API

### Install uv - Rust based Python packager (windows)
``` winget install --id=astral-sh.uv  -e ```

### Project Setup 
```
uv init 
uv venv
source .venv/bin/activate
uv add "mcp[cli]" httpx
```

### Run 
``` mcp dev server.py ```
- The MCP Inspector is available at http://127.0.0.1:6274
- Connect -> Tools -> List Tools -> get_current_weather
- Enter a latitude and longitude, eg 63.4463991, 10.8127596
- "Tool Result" -> you'll see a JSON object with weather data
