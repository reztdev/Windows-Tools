# Windows Tools Manager

A comprehensive Windows system management tool developed by **reztdev** that provides essential Windows administration features in a user-friendly GUI interface.

## 🔧 Features

### Core Functions
- **Windows Update Management**: Enable or disable Windows Update services completely
- **Windows/Office Activation**: Automated activation tool for Windows and Office products
- **Group Policy Editor (Gpedit)**: Enable Group Policy Editor on Windows Home editions
- **Sharing & Network Fix**: Repair folder and printer sharing functionality

### System Information Display
- Real-time system detection (OS, Architecture, Build)
- Hardware information (CPU, RAM with DDR type, GPU)
- Detailed process logging

## 🚀 Usage

### Initial Setup
1. **Administrator Privileges Required**: The application must be run as administrator to modify system settings
2. **License Authentication**: Enter the daily license code (8-digit code) provided by the developer
3. **Serial Number**: Your hardware serial is displayed for license key requests

### Main Operations

#### Windows Update Management
- **Disable Windows Update**: 
  - Stops all Windows Update services (wuauserv, UsoSvc, uhssvc, WaaSMedicSvc)
  - Disables scheduled tasks related to updates
  - Removes SoftwareDistribution directory
  - Modifies registry settings to prevent automatic updates

- **Enable Windows Update**:
  - Restores all Windows Update services
  - Re-enables scheduled tasks
  - Restores original registry settings
  - Allows normal Windows Update functionality

#### Windows/Office Activation
- Automated activation process for Windows and Office products
- Uses PowerShell-based activation methods
- No manual key entry required

#### Enable Group Policy Editor (Gpedit)
- Enables Group Policy Editor on Windows Home editions
- Uses DISM to install required packages:
  - Microsoft-Windows-GroupPolicy-ClientExtensions-Package
  - Microsoft-Windows-GroupPolicy-ClientTools-Package
- Requires system restart after completion

#### Fix Sharing (Folder & Printer)
- Repairs common network sharing issues
- Enables SMB protocols (SMB1Protocol, SMB1Protocol-Client, SMB1Protocol-Server)
- Configures registry settings for guest authentication
- Starts essential services:
  - TCP/IP NetBIOS Helper (lmhosts)
  - Server (File & Printer Sharing)
  - Workstation service
- Requires system restart for full effect

#### Ghost ToolBox (More Features)
- Author : https://github.com/Batlez/Ghost-Toolbox

## 🛡️ Security Features

### License Protection
- Daily license code system using HMAC-SHA256 authentication
- Hardware-based serial number (HWID) binding
- Rate limiting: 5 attempts with 30-second lockout
- Contact developer with your serial number for license codes

### Single Instance Protection
- Prevents multiple instances of the application running simultaneously
- Uses Windows mutex for process management

## 📋 System Requirements

- **Operating System**: Windows 8/8.1/10/11 (32-bit or 64-bit)
- **Privileges**: Administrator rights required
- **Internet Connection**: Required for downloading utilities and activation processes

## 🔍 Process Logging

The application provides detailed logging for all operations:
- Real-time process monitoring
- Error reporting and troubleshooting information
- Success/failure status for each operation
- Clear log functionality for fresh starts

## ⚠️ Important Notes

### Before Using Windows Update Disable:
- **Create a system restore point** before disabling Windows Update
- Some Windows features may require updates to function properly
- Security updates will not be installed automatically

### Restarting Required:
- Group Policy Editor enablement
- Network sharing fixes
- Some registry modifications

### Antivirus Software:
- Some antivirus programs may flag system modification tools
- Temporarily disable real-time protection if needed
- The application is safe and does not contain malware

## 🆘 Troubleshooting

### Common Issues:
1. **"Administrator Required" Error**: Right-click the executable and select "Run as administrator"
2. **License Code Invalid**: Contact the developer with your displayed serial number
3. **Services Won't Stop**: Some services may be in use by other processes - try restarting Windows first
4. **Registry Access Denied**: Ensure you're running as administrator and no group policies are blocking access

### Getting License Codes:
- Display your hardware serial number from the license window
- Contact the developer via GitHub: [@reztdev](https://github.com/reztdev)
- Provide your serial number to receive daily license codes

## 📞 Support & Contact

- **Developer**: reztdev
- **GitHub**: [https://github.com/reztdev](https://github.com/reztdev)
- **License Support**: Provide your hardware serial number for license key requests

## ⚖️ Disclaimer

This tool modifies Windows system settings and services. Use at your own risk. The developer is not responsible for any system damage or data loss. Always create backups before making system modifications.

---

*Windows Tools Manager - Simplifying Windows Administration*
