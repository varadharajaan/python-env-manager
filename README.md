# Environment Manager

A cross-platform Python environment management tool for Windows.

## Features

- **Conda environment management** - Create, delete, switch, and list conda environments
- **Virtual environment support** - Manage Python venvs
- **PowerShell integration** - Wrapper scripts for easy activation
- **Copy-jar utility** - Helper for copying JAR files (JetBrains tools)

## Files

| File | Description |
|------|-------------|
| `env_manager.py` | Main Python script (2000+ lines) |
| `env_manager.ps1` | PowerShell wrapper with menu |
| `env_manager_wrapper.ps1` | Alternative wrapper |
| `env_wrapper.ps1` | Simplified wrapper |
| `activate_conda.ps1` | Conda activation helper |
| `activate_env.ps1` | Environment activation helper |
| `copy-jar.py` | JAR file copy utility |
| `copy-jar.ps1` | PowerShell wrapper for copy-jar |

## Usage

```powershell
# Interactive menu
.\env_manager.ps1

# Direct Python usage
python env_manager.py --help
python env_manager.py list
python env_manager.py create myenv
python env_manager.py switch myenv
python env_manager.py delete myenv
```

## Documentation

See [ENV_MANAGER_GUIDE.md](ENV_MANAGER_GUIDE.md) for detailed usage instructions.
