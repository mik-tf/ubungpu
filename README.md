<h1> Ubungpu - Ubuntu GPU Setup Tool</h1>

<h2> Table of Contents</h2>

- [Introduction](#introduction)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
  - [Manual Installation](#manual-installation)
  - [Using Make](#using-make)
- [Usage](#usage)
- [Commands](#commands)
- [Examples](#examples)
- [Logging](#logging)
- [License](#license)
- [Support](#support)

## Introduction

Ubungpu is a comprehensive GPU setup tool for Ubuntu systems with NVIDIA or AMD graphics cards. It automates the installation and configuration of GPU drivers and toolkits, making GPU setup simple and reliable.

## Features

- Automated NVIDIA and AMD driver installation
- CUDA and ROCm toolkit setup
- System compatibility checks
- Detailed logging system
- GPU status monitoring
- Interactive installation process
- Command-line interface
- Secure execution model

## Requirements

- Ubuntu operating system (20.04 or newer recommended)
- NVIDIA or AMD GPU
- Sudo privileges
- Internet connection
- Basic system utilities

## Installation

### Manual Installation

```bash
# Download
wget https://raw.githubusercontent.com/mik-tf/ubungpu/main/ubungpu.sh

# Install
bash ubungpu.sh install

# Remove installer
rm ubungpu.sh
```

### Using Make

The project includes a Makefile for easier management. Available make commands:

```bash
# First clone the repository
git clone https://github.com/mik-tf/ubungpu
cd ubungpu

# Install the tool
make build

# Reinstall (uninstall then install)
make rebuild

# Remove the installation
make delete
```

The Makefile commands do the following:
- `make build`: Installs the script system-wide
- `make rebuild`: Removes existing installation and reinstalls
- `make delete`: Removes the installation completely

## Usage

Run the command with no arguments to see help:
```bash
ubungpu
```

## Commands

- `build` - Run full GPU setup
- `status` - Show GPU status
- `install` - Install script system-wide
- `uninstall` - Remove script from system
- `logs` - Show full logs
- `recent-logs [n]` - Show last n lines of logs
- `delete-logs` - Delete all logs
- `help` - Show help message
- `version` - Show version information

## Examples

```bash
# Run full setup
ubungpu build

# Check GPU status
ubungpu status

# View logs
ubungpu logs

# Show recent logs
ubungpu recent-logs 100
```

## Logging

Logs are stored in `/var/log/ubungpu/` with the following features:
- Installation logging
- Error tracking
- Status updates
- Timestamp information
- Log rotation
- Cleanup utilities

## License

Apache License 2.0

## Support

For issues and questions:
[GitHub Repository](https://github.com/mik-tf/ubungpu)
