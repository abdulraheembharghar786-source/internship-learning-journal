# Week 2 - Session 3
## 1. GitHub Connectivity & Branching
Connecting local machine ↔ GitHub via CLI or GitHub Desktop.

Branching:

Useful for collaboration and feature isolation.

Not strictly required for solo projects.

Branches can be deleted or kept private.

Pulling repositories into CLI/WSL and opening them in VS Code works seamlessly if Git is configured.

## 2. WSL & VS Code Integration
Git configuration in WSL persists when accessed via VS Code.

Virtual environments:

Best practice to avoid global installs.

Windows vs WSL environments differ; recreate via requirements.txt if needed.

VS Code can connect to WSL using the Remote – WSL extension.

## 3. SSH Keys
One SSH setup per machine is sufficient.

Works across all repositories once configured.

## 4. GitHub Codespaces
Cloud-hosted development environment.

Access via:

Browser UI

VS Code

CLI

Offers configurable machines (2–32 cores, 8–128 GB RAM).

Free tier: 120 hours/month (GitHub Free), 180 hours/month (GitHub Pro via student pack).

Auto-shutdown after 30 minutes inactivity.

Repository setup:

.devcontainer/ folder

devcontainer.json for configuration

Optional Dockerfile for dependencies

Supports multiple configurations for different teams (e.g., dev vs testing).

## 5. Repository Size Limits
GitHub account storage: ~15 GB total.

File size limit: 100 MB (use Git LFS for larger files).

Recommended repo size: ≤1 GB for performance.

## 6. Hugging Face Spaces
Platform for deploying ML models and datasets.

Supports cloning repos with Git LFS for large files.

Models often include large tensor files (GBs in size).

Free accounts available; similar to GitHub but focused on ML.

💻 GitHub Code Example
You can save these notes in a repo as SESSION3_NOTES.md:

markdown

## GitHub Connectivity
- CLI & Desktop connections
- Branching for collaboration
- SSH setup once per machine

## WSL & VS Code
- Git config persists in WSL
- Use virtual environments
- Remote – WSL extension for VS Code

## GitHub Codespaces
- Cloud dev environment
- Access via UI, VS Code, CLI
- Configurable cores/RAM
- Free tier: 120–180 hrs/month
- `.devcontainer/` folder with JSON + Dockerfile

## Repository Limits
- 15 GB total storage
- 100 MB per file (use Git LFS)
- Recommended repo size ≤1 GB

## Hugging Face Spaces
- Deploy ML models/datasets
- Git LFS required for large files
- Free accounts available
