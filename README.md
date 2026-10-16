# Intune-Entra Endpoint Management Lab

## Objective

Configured a Windows 11 Pro virtual machine and integrated Microsoft Entra ID and Microsoft Intune to practice cloud-based endpoint management. This lab focuses on device enrollment, security policy deployment, application management, and compliance validation.

## Technologies Used

- Oracle VirtualBox
- Windows 11 Pro
- Microsoft Intune
- Microsoft Entra ID
- PowerShell
- Microsoft Win32 Content Prep Tool
- 7-Zip

## Architecture

Microsoft Entra ID provides device identity and join capabilities, while Microsoft Intune manages device configuration, application deployment, and compliance.

**Environment flow:**

Microsoft Entra ID → Windows 11 device identity and join

Microsoft Intune → Device management, configuration policies, application deployment, and compliance

Windows 11 Pro VM → Enrolled endpoint used for testing and validation

## Tasks Performed

### Device Enrollment & Management

- Joined a Windows 11 Pro virtual machine to Microsoft Entra ID.
- Enrolled the device in Microsoft Intune.
- Verified the device join type and Intune management status.

### Configuration Policy

- Created and deployed a Windows firewall configuration policy named `CFG-WIN-Firewall`.
- Configured Domain, Private, and Public firewall profiles to be enabled.
- Configured default inbound traffic to be blocked and outbound traffic to be allowed.
- Validated the effective firewall settings using PowerShell.

### Application Deployment

- Packaged the 7-Zip x64 installer using Microsoft's Win32 Content Prep Tool.
- Configured 7-Zip as a Win32 application in Microsoft Intune.
- Configured silent installation, application requirements, detection rules, and assignment to a test-user security group.
- Verified that Intune reported the application as Installed.

### Compliance Management

- Created a Windows compliance policy named `COMP-WIN-Baseline`.
- Configured the policy to require Windows Firewall to be enabled.
- Assigned the policy to the test-user security group.
- Verified that the Windows 11 device reported as Compliant in Intune.

### Troubleshooting

- Investigated and resolved an initial device enrollment issue (`8018000a`).
- Validated device enrollment, policy deployment, application installation, and compliance reporting.
- Documented configuration steps and validation results.

## Project Documentation

Detailed configuration, validation, and troubleshooting documentation is organized by project:

| Project                                              | Topic                                                             |
| ---------------------------------------------------- | ----------------------------------------------------------------- |
| [Device Enrollment](01-Device-Enrollment/)           | Microsoft Entra device join and Intune enrollment.                |
| [Configuration Policy](02-Configuration-Policy/)     | Firewall policy configuration and PowerShell validation.          |
| [Application Deployment](03-Application-Deployment/) | 7-Zip packaging, deployment, and detection.                       |
| [Compliance](04-Compliance/)                         | Compliance policy configuration and device compliance validation. |
| [Troubleshooting](05-Troubleshooting/)               | Enrollment error investigation and resolution.                    |
