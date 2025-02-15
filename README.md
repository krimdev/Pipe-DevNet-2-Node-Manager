# Pipe DevNet 2 Node Manager

A bash script to manage Pipe DevNet 2 nodes easily. This script provides a user-friendly interface to install, configure, and manage your Pipe node.

## Features

- Easy installation and configuration
- Referral code support during installation
- Solana wallet address validation
- Configurable RAM and disk space allocation
- Custom cache directory support
- Node status monitoring
- Service management (start/stop)
- Backup management
- Easy uninstallation
- Referral code generation

## Requirements

- Linux operating system
- Sudo privileges
- Minimum 4GB RAM
- At least 100GB free disk space
- Internet connectivity available 24/7

## Installation

1. Download the script:
```bash
wget https://raw.githubusercontent.com/krimdev/Pipe-DevNet-2-Node-Manager/main/pipe-manager.sh
```

2. Make it executable:
```bash
chmod +x pipe-manager.sh
```

3. Run the script:
```bash
./pipe-manager.sh
```

## Usage

The script provides an interactive menu with the following options:

1. Install/Start/Stop node
2. Show status
3. Generate referral code
4. Backup node
5. Update node
6. Configure node
7. Uninstall node
8. Exit

### Initial Setup

During the first installation, you'll need to provide:
- Your Solana wallet address
- RAM allocation (default: 8GB)
- Disk space allocation (default: 200GB)
- Cache directory location
- Referral code (optional)

### Configuration

You can modify your node's configuration at any time using option 6:
- Change Solana wallet address
- Adjust RAM allocation
- Modify disk space allocation
- Update cache directory location

### Service Management

The node runs as a systemd service for reliability. The script manages this automatically, but you can also manually control it:
```bash
sudo systemctl start pop.service
sudo systemctl stop pop.service
sudo systemctl status pop.service
```

### Logs

View node logs using:
```bash
sudo journalctl -u pop.service
```

### Backup

The script automatically creates backups of your node_info.json file during important operations. Backups are stored in your home directory with timestamps.

## Support

For issues with the script, please open an issue on GitHub.

For Pipe Network related questions, visit:
- [Dashboard](https://dashboard.pipenetwork.com/node-lookup)
- [Official Documentation](https://docs.pipenetwork.com)

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## Author

Created by KrimDev

## License

MIT License - see the [LICENSE.md](LICENSE.md) file for details
