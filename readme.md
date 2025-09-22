# Develop AI Agents in Azure

The exercises in this repo are designed to provide you with a hands-on learning experience in which you'll explore common tasks that developers perform when building AI agents on Microsoft Azure.

> **Note**: To complete the exercises, you'll need an Azure subscription in which you have sufficient permissions and quota to provision the necessary Azure resources and generative AI models. If you don't already have one, you can sign up for an [Azure account](https://azure.microsoft.com/free). There's a free trial option for new users that includes credits for the first 30 days.

View the exercises in the [GitHub Pages site for this repo](https://go.microsoft.com/fwlink/?linkid=2310820).

> **Note**: While you can complete these exercises on their own, they're designed to complement modules on [Microsoft Learn](https://learn.microsoft.com/training/paths/develop-ai-agents-on-azure/); in which you'll find a deeper dive into some of the underlying concepts on which these exercises are based.

## Running in a Dev Container

To run the exercises in a Dev Container, follow these steps:

1. Open the repository in Visual Studio Code.
2. Press `F1` and select `Remote-Containers: Reopen in Container`.
3. Wait for the container to build and start.
4. Open a terminal in the container.
5. Start the virtual environment by running the following command:
   ```
   source .venv/bin/activate
   ```

### Dev Container Configuration Updates

The following updates have been made to fix dev container build issues:

#### **Changed Python Version (September 2025)**
- **Changed from**: Python 3.13 (Debian trixie)
- **Changed to**: Python 3.12 (Debian bookworm)
- **Reason**: Python 3.13 uses unstable Debian "trixie" which lacks Azure CLI repository support

#### **Fixed Workspace Path References**
- **Updated**: All `/workspaces/ai-agents/` references to `/workspaces/mslearn-ai-agents/`
- **Files affected**: 
  - `.devcontainer/devcontainer.json` (postCreateCommand, Python interpreter path)
  - `.devcontainer/setup-venvs.sh` (virtual environment and Labfiles paths)

#### **Fixed JSON Configuration Issues**
- **Fixed**: `editor.defaultFormatter` setting (changed from invalid ESLint reference to `null`)
- **Fixed**: `source.fixAll.eslint` setting (changed from boolean `true` to string `"explicit"`)

#### **Fixed Directory Creation Issues**
- **Added**: `sudo mkdir -p /usr/local/python/current/bin` to postCreateCommand
- **Reason**: Prevents symlink creation failures when target directories don't exist

#### **Removed Redundant Features**
- **Removed**: `ghcr.io/devcontainers/features/python:1` from features list
- **Reason**: Python 3.12 base image already includes Python, avoiding conflicts
   
## Reporting issues

If you encounter any problems in the exercises, please report them as **issues** in this repo.


