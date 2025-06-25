# VMware Tools Removal Script

## Overview

This PowerShell script provides a comprehensive method to forcefully remove VMware Tools from Windows systems when standard uninstallation methods fail. It's particularly useful during VM migrations (e.g., VMware to Hyper-V) or when VMware Tools becomes corrupted.

## Credits

- **Original Author**: [@broestls](https://github.com/broestls)
- **Original Source**: [GitHub Gist](https://gist.github.com/broestls/f872872a00acee2fca02017160840624)
- **Modifications**: Syntax fixes for Windows 10 compatibility

## ⚠️ Important Warnings

**This script will remove ALL VMware-related components, including:**
- VMware Tools
- VMware Workstation Pro (if installed)
- All VMware services
- All VMware registry entries
- VMware program files and common files

**If you only want to remove VMware Tools while keeping VMware Workstation Pro, use Windows "Add or Remove Programs" instead.**

## Requirements

- Windows PowerShell 5.0 or later
- Administrator privileges
- Windows 2008-2019 (tested), Windows 10/11 (compatible)
- System reboot required after completion

## What the Script Does

1. **Identifies VMware Tools**: Searches registry for VMware Tools installer IDs
2. **Stops Services**: Halts all running VMware services
3. **Removes Services**: Deletes VMware services from the system
4. **Cleans Registry**: Removes all VMware-related registry entries
5. **Deletes Files**: Removes VMware program files and common files
6. **Confirmation**: Asks for user confirmation before proceeding

## Usage

### Method 1: Run Directly
```powershell
# Open PowerShell as Administrator
# Navigate to script directory
cd "D:\R&D\DevOps-Cyber\Projects\self-projects\Homelab-project\Homelab-private\scripts\Vmware Removal Tool"

# Execute the script
.\Remove_VMwareTools.ps1
```

### Method 2: Remote Execution
```powershell
# For remote systems (requires PSRemoting)
Invoke-Command -ComputerName "TargetPC" -FilePath ".\Remove_VMwareTools.ps1"
```

## Script Output

The script will display:
- List of registry keys to be deleted
- List of filesystem folders to be deleted  
- List of services to be stopped/removed
- Confirmation prompt (requires 'y' to proceed)
- Progress messages during execution
- Completion message with reboot reminder

## Common Use Cases

### 1. VMware to Hyper-V Migration
When migrating VMs from VMware to Hyper-V, VMware Tools can cause conflicts and should be removed.

### 2. Corrupted VMware Tools
When VMware Tools installation becomes corrupted and won't uninstall normally.

### 3. Clean System Preparation
Before installing different virtualization guest additions.

## Alternative Methods

Based on the [GitHub Gist discussions](https://gist.github.com/broestls/f872872a00acee2fca02017160840624), there are alternative approaches:

### MSI Repair Method
For VMware Tools version 12 that fails to uninstall in Hyper-V:
1. Locate the cached MSI file in `C:\Windows\Installer`
2. Use Orca to remove the `VM_LogStart` action from the CustomAction table
3. Save and replace the MSI file
4. Run standard uninstall

### Registry-Only Approach
Some users prefer to only clean specific registry keys without removing all VMware components.

## Troubleshooting

### Script Doesn't Find VMware Tools
- Verify VMware Tools is actually installed
- Check if it appears in "Add or Remove Programs"
- Run script as Administrator

### Services Won't Stop
- Manually stop VMware services first
- Use `services.msc` to identify running VMware services
- Restart in Safe Mode if necessary

### Registry Access Denied
- Ensure running as Administrator
- Check if registry keys are protected
- Some enterprise environments may restrict registry access

## Files Removed

The script targets these locations:
- `C:\Program Files\VMware\`
- `C:\Program Files\Common Files\VMware\`
- Registry keys under `HKEY_CLASSES_ROOT\Installer\`
- Registry keys under `HKLM:\SOFTWARE\`
- VMware services and their registry entries

## Post-Execution Steps

1. **Reboot Required**: Always reboot after running the script
2. **Verify Removal**: Check that VMware entries are gone from:
   - Add or Remove Programs
   - Services (services.msc)
   - Device Manager (for any remaining VMware devices)
3. **Install New Guest Additions**: If migrating to another hypervisor

## Version History

- **Original**: Created by @broestls for Windows Server environments
- **Current**: Modified for Windows 10 compatibility with syntax fixes

## License

This script is provided as-is for educational and administrative purposes. Use at your own risk.

## Support

For issues or questions:
- Check the [original GitHub Gist](https://gist.github.com/broestls/f872872a00acee2fca02017160840624) for community discussions
- Review VMware documentation for standard uninstall procedures
- Consider the MSI repair method for VMware Tools v12 issues 