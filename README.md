# Microsoft 365 & Azure Help Desk Administration Lab

## Project Overview

This project demonstrates hands-on experience administering a simulated corporate Microsoft 365 environment for NovaTech Solutions.

I configured Microsoft Entra ID, Exchange Online, Microsoft Intune, and Microsoft 365 administrative services to practice common Tier 1 and Tier 2 IT support responsibilities.

The lab includes user provisioning, license management, security groups, MFA policy configuration, shared mailbox administration, device enrollment, compliance troubleshooting, password resets, and employee onboarding/offboarding.

**Environment:** Microsoft 365 Business Premium Trial  
**Organization:** NovaTech Solutions  
**Tenant:** `novatechhelpdesk.onmicrosoft.com`  
**Device:** Windows 11 Pro on Oracle VirtualBox

## Technologies Used

- Microsoft 365 Admin Center
- Microsoft Entra ID (Azure Active Directory)
- Microsoft Exchange Online
- Microsoft Intune
- Microsoft Defender Antivirus
- Conditional Access
- Microsoft Authenticator
- Windows 11 Pro
- Oracle VirtualBox

## 1. Microsoft 365 Tenant and User Administration

Configured a Microsoft 365 Business Premium tenant and provisioned eight fictional employee accounts across IT, Human Resources, Finance, and Sales.

Assigned Microsoft 365 licenses and maintained standard user permissions.

### Microsoft 365 Admin Dashboard

![Microsoft 365 Admin Center](screenshots/01-Microsoft-365-Admin-Dashboard.png)

### User Creation

![User Creation](screenshots/02-Microsoft-365-User-Creation.png)

### Active Users

![Active Users](screenshots/03-Microsoft-365-Active-Users.png)

### Department Employees

![Employee Accounts](screenshots/04-Microsoft-365-Employee-Accounts.png)

## 2. Microsoft Entra ID — Identity and Access Management

Created departmental security groups and configured assigned membership to organize user access.

**Security Groups:**
- SG-IT-Staff
- SG-HR-Staff
- SG-Finance-Staff
- SG-Sales-Staff

### Microsoft Entra Dashboard

![Microsoft Entra Dashboard](screenshots/05-Microsoft-Entra-Dashboard.png)

### Security Groups

![Security Groups](screenshots/06-Entra-Security-Groups.png)

### Group Membership

![Group Membership](screenshots/07-Entra-Group-Membership.png)

## 3. Multi-Factor Authentication and Conditional Access

Configured Microsoft Authenticator as an authentication method for IT employees.

Created a Conditional Access policy targeting the IT security group.

**Policy Configuration:**
- Policy: `CA-Require-MFA-IT-Users`
- Target: SG-IT-Staff
- Resources: All resources
- Grant control: Require multifactor authentication
- Policy state: Report-only

The policy was evaluated in Report-only mode without enforcing MFA through that policy.

### Authentication Methods

![MFA Authentication Methods](screenshots/08-MFA-Authentication-Methods.png)

### Conditional Access Policy

![Conditional Access Policy](screenshots/09-Conditional-Access-Policy.png)

### Conditional Access Configuration

![Conditional Access Configuration](screenshots/10-Conditional-Access-Configuration.png)

## 4. Exchange Online Administration

Created an IT Support shared mailbox and configured delegated access for department employees.

**Shared Mailbox:** `support@novatechhelpdesk.onmicrosoft.com`

Configured:
- Full Access permissions
- Send As permissions
- Departmental email distribution list
- Internal distribution group membership

### Shared Mailbox

![Shared Mailbox](screenshots/11-Exchange-Shared-Mailbox.png)

### Full Access Permissions

![Full Access](screenshots/12-Shared-Mailbox-Full-Access.png)

### Send As Permissions

![Send As](screenshots/13-Shared-Mailbox-Send-As.png)

### Distribution List

![Distribution List](screenshots/14-Exchange-Distribution-List.png)

### Distribution List Members

![Distribution List Members](screenshots/15-Distribution-List-Members.png)

### Email Delivery Testing

![Distribution List Test](screenshots/16-Distribution-List-Email-Test.png)

## 5. Microsoft Intune Device Management

Configured automatic MDM enrollment for an assigned Microsoft Entra security group.

Created a Windows 11 Pro virtual machine and joined it to Microsoft Entra ID.

Verified that the workstation was successfully managed through Microsoft Intune.

**Device Name:** `M365-WIN01`  
**Operating System:** Windows 11 Pro  
**Primary User:** James Wilson  
**Management Platform:** Microsoft Intune

### Intune Dashboard

![Intune Dashboard](screenshots/17-Intune-Device-Dashboard.png)

### Automatic Enrollment

![Automatic Enrollment](screenshots/18-Intune-Automatic-Enrollment.png)

### Windows Virtual Machine

![Windows VM](screenshots/19-Intune-Windows-VM.png)

### Microsoft Entra Device Join

![Entra Device Join](screenshots/20-Microsoft-Entra-Device-Join.png)

### Intune Device Enrollment

![Intune Device Enrollment](screenshots/21-Intune-Device-Enrollment.png)

## 6. Device Compliance and Troubleshooting

Created a Windows device compliance policy to enforce fundamental endpoint security requirements.

**Policy:** `Windows 11 - Corporate Compliance`

Configured requirements for:
- Windows Firewall
- Antivirus
- Antispyware
- Microsoft Defender Antimalware
- Real-time protection
- Up-to-date Defender security intelligence

Initially encountered a noncompliant device status caused by outdated Microsoft Defender security intelligence.

Investigated the failed compliance setting, updated Defender security intelligence, synchronized the device, and verified that the workstation returned to a compliant state.

### Compliance Policy

![Compliance Policy](screenshots/22-Intune-Compliance-Policy.png)

### Successful Compliance Verification

![Intune Compliance](screenshots/23-Intune-Compliance-Verification.png)

## 7. Help Desk Password Reset

Simulated an employee password reset request through the Microsoft 365 Admin Center.

Reset a fictional employee's password, configured a temporary password, and required a password change at the next sign-in.

### Password Reset

![Microsoft 365 Password Reset](screenshots/24-Microsoft-365-Password-Reset.png)

## 8. Employee Onboarding

Simulated onboarding a new employee, Kevin Anderson, in the Sales department.

Completed:
- Microsoft 365 user provisioning
- Department and job title configuration
- Business Premium license assignment
- Security group membership
- Standard user permission assignment

### Employee Onboarding

![Employee Onboarding](screenshots/25-Microsoft-365-Employee-Onboarding.png)

### Security Group Assignment

![Security Group Assignment](screenshots/26-Employee-Group-Assignment.png)

## 9. Employee Offboarding

Simulated offboarding the same fictional employee by:

1. Blocking Microsoft 365 sign-in.
2. Revoking active sign-in sessions.
3. Removing the employee from the Sales security group.
4. Removing the Microsoft 365 Business Premium license.

### Block User Sign-in

![Blocked Sign-In](screenshots/27-Employee-Sign-In-Blocked.png)

### Revoke Sessions

![Session Revocation](screenshots/28-Employee-Session-Revocation.png)

### Group Membership Removal

![Group Removal](screenshots/29-Employee-Group-Removal.png)

### License Removal

![License Removal](screenshots/30-Employee-License-Removal.png)

## Skills Demonstrated

- Microsoft 365 Administration
- Microsoft Entra ID Identity Management
- User Provisioning and License Management
- Security Group Administration
- Multi-Factor Authentication Configuration
- Conditional Access Policy Configuration
- Exchange Online Shared Mailbox Management
- Mailbox Delegation and Distribution Lists
- Microsoft Intune Device Enrollment
- Windows Endpoint Management
- Device Compliance Troubleshooting
- Microsoft Defender Security Intelligence Updates
- Employee Onboarding and Offboarding
- IT Help Desk Password Resets
- Technical Troubleshooting and Documentation

## Project Outcome

Successfully built a cloud-based Microsoft 365 IT administration lab using Microsoft Entra ID, Exchange Online, and Microsoft Intune.

Provisioned fictional employee accounts, configured identity and access management policies, managed shared mailboxes and distribution lists, enrolled a Windows 11 device, and resolved an actual Microsoft Intune compliance issue.

Completed hands-on employee onboarding, offboarding, and password reset procedures to demonstrate practical IT Help Desk and cloud administration skills.
