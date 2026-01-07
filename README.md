# Browser Use

Make websites accessible for AI agents.

## Overview

Browser Use is a powerful library designed to enable AI agents to autonomously interact with web browsers. It provides a robust set of tools for navigating, interacting with elements, and extracting information from the web using modern LLMs.

## Key Features

- **Autonomous Navigation**: Agents can navigate complex websites using Chromium via CDP.
- **LLM Integration**: Works with major LLM providers including OpenAI, Anthropic, Google, and Groq.
- **DOM Processing**: Advanced DOM extraction and processing for better agent reasoning.
- **Event-Driven Architecture**: Fast and reliable browser management.

## Installation

```bash
uv add browser-use
```

## Quickstart

```python
from browser_use import Agent, Browser, ChatBrowserUse
import asyncio

async def main():
    browser = Browser()
    llm = ChatBrowserUse()

    agent = Agent(
        task="Find the latest news about AI",
        llm=llm,
        browser=browser,
    )

    await agent.run()

if __name__ == "__main__":
    asyncio.run(main())
```

## Author

Developed and maintained by [daniellopez882](https://github.com/daniellopez882).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
