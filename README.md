# Valo Stretched Tool

Automatically configure stretched resolution for Valorant with interactive menu.

## Features

### Toggle Resolution
- Quick switch between stretched and native resolution
- Save configurations to config.ini
- Support custom resolutions

### Auto-Configure Stretched
- Automatically configure GameUserSettings.ini
- Apply to both generic and user-specific settings
- Auto-copy template if needed

### Monitor RiotLocalMachine.ini
- Auto-check every 5 seconds
- Detect LastKnownUser changes
- Alert with sound notification

### Check Stretched Status
- Show green: "Da stretched" (all settings correct)
- Show red: "Chua stretched" (needs configuration)

## Requirements

- Windows 10/11
- PowerShell 5.0+ (built-in)
- Valorant installed

## Usage

1. Double-click **RunTool.bat**
2. Select from menu:
   - 1: Toggle resolution
   - 2: Change stretched ratio
   - 3: Enable/Disable monitoring
   - 4: Run stretched (auto-configure)
   - 0: Exit

## Configuration

Edit **config.ini**:
```ini
stretched = 1440x1080
native = 1920x1080
```

## File Structure

```
valo-stretched-tool/
├── StretchedTool.ps1
├── RunTool.bat
├── config.ini
├── GameUserSettings.ini
└── README.md
```

## Troubleshooting

### Cannot find User ID
- Ensure Valorant has been run at least once
- Verify RiotLocalMachine.ini exists

### Always shows "Chua stretched"
- Run option 4 to auto-configure GameUserSettings.ini

### Script won't run
Enable PowerShell execution:
```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

## Portability

100% portable - works anywhere:
- Copy to different folder: works
- Copy to different PC: works
- No admin required
- No registry changes
- Relative paths only

## License

MIT License - Free to use, modify, and distribute

---

Made with heart for Valorant players
