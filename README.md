# Open Swiss Model Context Protocol

![vc3598_A_typical_scene_of_natural_Switzerland_with_a_swiss_trai_867174fe-a627-4ea9-af22-5025026780a5](https://github.com/user-attachments/assets/7f105fa3-1db4-411b-aee4-448e268fc0a6)

[![PyPI version](https://badge.fury.io/py/osmcp.svg)](https://badge.fury.io/py/osmcp)
[![CI](https://github.com/grll/OpenSwissMCP/actions/workflows/ci.yml/badge.svg)](https://github.com/grll/OpenSwissMCP/actions/workflows/ci.yml)
[![GitHub stars](https://img.shields.io/github/stars/grll/OpenSwissMCP.svg)](https://github.com/grll/OpenSwissMCP/stargazers)
[![License](https://img.shields.io/github/license/grll/OpenSwissMCP.svg)](https://github.com/grll/OpenSwissMCP/blob/main/LICENSE)

<!--
[![Downloads](https://pepy.tech/badge/osmcp)](https://pepy.tech/project/osmcp)
-->

Open Swiss MCP connects Large Language Models to Switzerland's open data infrastructure through Anthropic's Open Source Model Context Protocol. This enables any LLMs to provide real-time, data-grounded responses about Swiss public services and informations.

## Why Open Swiss MCP?

- **Rich Data Source**: Access to 12,000+ high-quality datasets from opendata.swiss, Switzerland's official open data platform.
- **Real-Time Insights**: Get accurate answers about Swiss public services (weather, transport, etc.)
- **Simple Integration**: Built on Anthropic's Model Context Protocol for seamless LLM integration with any supported clients.
- **Open Architecture**: Designed for community contribution and dataset expansion.

## Key Features

- One-Command setup
- Access to Swiss public datasets (incl. SBB real-time train informations, Weather updates...)
- Compatible with Claude and other MCP-enabled LLMs Application

We maintain a strong focus on reliability, simplicity, and extensibility. Contributions to expand the supported datasets are welcome!

## Usage

### Prerequisites

If you want to use Open Swiss MCP with Claude Desktop app client you need to install the [Claude Desktop app](https://claude.ai/download).

You will also need `uv` to easily run our CLI and MCP servers.

#### macOS & Linux

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

#### Windows

```bash
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

### Open Swiss MCP - CLI Tool

#### Overview

```bash
# show available commands
uvx osmcp 

# show available providers
uvx osmcp list

# show info about a provider
uvx osmcp info $PROVIDER_NAME

# setup a provider's MCP server on your Claude Desktop app
uvx osmcp setup $PROVIDER_NAME

# remove a provider's MCP server from your Claude Desktop app
uvx osmcp remove $PROVIDER_NAME
```

#### Example

Quickstart for the SBB provider:

```bash
uvx setup sbb
```

## Contributing

We want to scale!

* keep things as simple as possible -> toward AI generated pages keep things in single file
* keep things as standard as possible (TOOLS, TOOLS_HANDLER) and follow the guidelines for what should be a tool, what should be a resource...
* keep it as low as possible in external dependencies (weigh always pros / cons of integrating a new dependency with always a bias toward not adding it)
* keep things formatted with ruff
* keep things tested with pytest
* use typehints and pydantic model for input output of api requests

Concretly:
brew install uv / or other mean to install uv
git clone
uv venv
uv sync
pre-commit install
## Roadmap

data extension
1. integrate as many sources as possible from opendata.swiss

framework extension
1. add support for 

## Limitations
* please oblige to the license must be quoted in commercial application
* please oblige to the license of the data providers

## References
* Model Context Protocol (Anthropic)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
