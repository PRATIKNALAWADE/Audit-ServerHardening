# Security Audit and Hardening Script

---

This script automates security audits and server hardening processes for Linux servers. It performs comprehensive checks, identifies vulnerabilities, and applies hardening measures to improve server security.

## Features

- **User and Group Audits**: List users/groups, check for UID 0 users, and identify users with weak or no passwords.
- **File and Directory Permissions**: Scan for world-writable files/directories and SUID/SGID files.
- **Service Audits**: List running services and check for unnecessary or unauthorized services.
- **Firewall and Network Security**: Verify firewall status, report open ports, and check IP forwarding.
- **IP and Network Configuration Checks**: Identify public vs. private IP addresses.
- **Security Updates and Patching**: Check for available security updates and verify automatic update configurations.
- **Log Monitoring**: Check for suspicious log entries related to SSH.
- **Server Hardening**: Implement SSH key-based authentication, disable IPv6, secure the bootloader, configure the firewall, and set up automatic updates.
- **Custom Security Checks**: Extend the script with custom checks based on specific requirements.
- **Report and Alerting**: Generate a summary report of the audit and hardening process.

## Installation

### Prerequisites

Ensure you have the following packages installed on your Linux server:

1. **Update Package Lists**:
    
    ```bash
    sudo apt update
    
    ```
    
2. **Install Required Packages**:
    
    ```bash
    sudo apt install -y net-tools procps sysstat gawk ufw iptables grub2 unattended-upgrades openssh-client openssh-server
    
    ```
    

### Clone the Repository

1. **Clone the Repository**:
    
    ```bash
    git clone <https://github.com/your-repo/security-audit.git>
    cd security-audit
    
    ```
    

### Set Script Permissions

1. **Make the Script Executable**:
    
    ```bash
    chmod +x security_audit.sh
    
    ```
    

## Configuration

### Custom Security Checks

- **Edit Configuration File**:
    - Open `security_checks.conf` in a text editor.
    - Add any custom security checks based on your organization’s requirements.

## Usage

### Running the Script

To execute the script and perform the security audit and hardening, run:

```bash
./security_audit.sh

```

## Example Output

### File and Directories Permission

![FileDirPermissions.png](FileDirPermission.png)

### Service Audit

![Audit.png](Audit.png)

## Troubleshooting

### Permissions Issues

- **Permission Denied**: If you encounter a "Permission Denied" error, ensure the script has execute permissions. Run:
    
    ```bash
    chmod +x security_audit.sh
    
    ```
    
- **Ownership**: Ensure you have the necessary permissions to execute the script. If needed, change ownership:
    
    ```bash
    sudo chown youruser:yourgroup security_audit.sh
    
    ```
    

### Common Errors

- **Missing Packages**: If certain commands are not found, ensure all required packages are installed.
- **Configuration Issues**: Verify that `security_checks.conf` is correctly formatted and contains valid commands.

## Documentation

### Script Details

The script is divided into modular functions for each security aspect, allowing for easy updates and customization:

- **User and Group Audits**
- **File and Directory Permissions**
- **Service Audits**
- **Firewall and Network Security**
- **IP and Network Configuration Checks**
- **Security Updates and Patching**
- **Log Monitoring**
- **Server Hardening**
- **Custom Security Checks**

### Configuration File

- **`security_checks.conf`**: A configuration file for adding custom security checks.

### Log File

- **`security_audit.log`**: The log file where audit results and actions are recorded.

## Contribution

Contributions are welcome! Please submit a pull request with improvements or updates.
