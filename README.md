# Python Environment Manager

A comprehensive Python environment management tool for Windows with support for multiple environment types.

[![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)](https://python.org)
[![Platform](https://img.shields.io/badge/Platform-Windows-blue.svg)](https://github.com/varadharajaan/python-env-manager)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## Features

### Environment Types Supported
- **Conda** - Full conda environment management
- **venv** - Python virtual environments
- **Poetry** - Poetry-managed environments
- **Pipenv** - Pipenv virtual environments
- **PDM** - PDM project environments
- **Hatch** - Hatch environments
- **pyenv** - pyenv Python versions
- **Docker** - Docker-based Python environments
- **Global Python** - System Python installations

### Core Capabilities
- 🔍 **Auto-discovery** - Automatically scans and detects all environment types
- 🔄 **Switch environments** - Seamlessly switch between environments
- 🗑️ **Delete environments** - Interactive deletion with multi-select support
- ✅ **Verify setup** - Check package manager availability with installation instructions
- 📊 **Multiple output formats** - Menu, Table, TUI, and JSON output
- 🎯 **Filter by type** - Scan only specific environment types
- 📁 **Project/Global scoping** - Scan project-local, global, or all environments

## Installation

```powershell
# Clone the repository
git clone https://github.com/varadharajaan/python-env-manager.git
cd python-env-manager

# No dependencies required - uses Python standard library only
```

## Requirements

- Python 3.7+
- Windows (PowerShell 5.1+)
- Optional: Conda, Poetry, Pipenv, PDM, Hatch, pyenv, Docker

## Usage

### PowerShell Wrapper (Recommended)

```powershell
# Interactive menu
.\env_manager.ps1
```

### Command Line

```powershell
# Show help
python env_manager.py --help

# List all environments (interactive menu)
python env_manager.py

# Different output formats
python env_manager.py --output table
python env_manager.py --output tui
python env_manager.py --output json

# Scan specific scope
python env_manager.py --scan project    # Local environments only
python env_manager.py --scan global     # Global environments only
python env_manager.py --scan all        # Both (default)

# Filter by environment type
python env_manager.py --type conda --type venv

# Specify project directory
python env_manager.py --project /path/to/project

# Switch between environments
python env_manager.py --switch

# Delete environments interactively
python env_manager.py --delete

# Deactivate current environment
python env_manager.py --deactivate

# Verify package managers are available
python env_manager.py --verify

# Enable debug logging
python env_manager.py --log-level DEBUG
```

## Files

| File | Description |
|------|-------------|
| `env_manager.py` | Main Python script with all functionality |
| `env_manager.ps1` | PowerShell wrapper with interactive menu |
| `env_manager_wrapper.ps1` | Alternative PowerShell wrapper |
| `env_wrapper.ps1` | Simplified wrapper |
| `activate_conda.ps1` | Conda activation helper |
| `activate_env.ps1` | Environment activation helper |
| `copy-jar.py` | JAR file copy utility (JetBrains tools) |
| `copy-jar.ps1` | PowerShell wrapper for copy-jar |

## Command Line Options

| Option | Description |
|--------|-------------|
| `--project`, `-p` | Project directory to scan (default: current) |
| `--output`, `-o` | Output format: `menu`, `table`, `tui`, `json` |
| `--scan` | Scope: `project`, `global`, `all` |
| `--type`, `-t` | Filter by type (repeatable) |
| `--only-project` | Disable global scanning |
| `--switch` | Switch between environments |
| `--delete` | Delete environments interactively |
| `--deactivate` | Deactivate current environment |
| `--verify` | Check package manager availability |
| `--log-level`, `-l` | Logging level (DEBUG, INFO, WARNING, ERROR) |

## Examples

```powershell
# List conda and venv environments in current project
python env_manager.py --type conda --type venv --scan project

# Get JSON output for automation
python env_manager.py --output json | ConvertFrom-Json

# Switch environments with type filter
python env_manager.py --switch --type conda

# Verify all package managers are installed
python env_manager.py --verify
```

## Documentation

See [ENV_MANAGER_GUIDE.md](ENV_MANAGER_GUIDE.md) for detailed usage instructions.

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

**Varadharajaan** - [GitHub](https://github.com/varadharajaan)
