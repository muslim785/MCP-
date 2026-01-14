# MCP-
# ubuntu2004 config --default-user root


### 
{
  "LOG": true,
  "LOG_LEVEL": "info",
  "HOST": "127.0.0.1",
  "PORT": 3456,
  "API_TIMEOUT_MS": 600000,

  "Providers": [
    {
      "name": "openrouter",
      "api_base_url": "https://openrouter.ai/api/v1/chat/completions",
      "api_key": "$OPENROUTER_API_KEY",
      "models": [
        "mistralai/devstral-2512:free"
      ],
      "transformer": {
        "use": ["openrouter"]
      }
    }
  ],

  "Router": {
    "default": "openrouter,mistralai/devstral-2512:free",
    "background": "openrouter,mistralai/devstral-2512:free",
    "think": "openrouter,mistralai/devstral-2512:free",
    "longContext": "openrouter,mistralai/devstral-2512:free",
    "longContextThreshold": 60000
  }
}

###
{
  "LOG": true,
  "LOG_LEVEL": "info",
  "HOST": "127.0.0.1",
  "PORT": 3456,
  "API_TIMEOUT_MS": 600000,
  "Providers": [
    {
      "name": "qwen",
      "api_base_url": "https://portal.qwen.ai/v1/chat/completions",
      "api_key": "key",
      "models": [
        "qwen3-coder-plus",
        "qwen3-coder-plus",
        "qwen3-coder-plus"
      ]
    }
  ],
  "Router": {
    "default": "qwen,qwen3-coder-plus",
    "background": "qwen,qwen3-coder-plus",
    "think": "qwen,qwen3-coder-plus",
    "longContext": "qwen,qwen3-coder-plus",
    "longContextThreshold": 60000,
    "webSearch": "qwen,qwen3-coder-plus"
  }
}
###
