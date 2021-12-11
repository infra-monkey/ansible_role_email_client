# Overview
This role installs and configures postfix to act as an MTA which enables sending email from the host.
This role requires root permissions. It must be called as root. This needs to be managed at the ansible or playbook level.

# Variables

| Name  | Type | Required | Default Value | Description |
| ----- | ---- | -------- | ------------- | ----------- |
| email_enabled | boolean | no | `false` | Is the host allowed to be an email client |
| email_address | string | no | `test@example.com` | The email address associated with the host |
| email_account | string | no | `test@example.com` | The email account associated with the host |
| email_password | string | no | `SuperPassw0rd` | The email account password associated with the host |
| relayhost | string | no | `smtp.example.com:25` | The relayhost to use for sending emails. Format is hostname:port |
| send_test_email | boolean | no | `false` | Send a test email at the end of the configuration |
| test_email_address | string | no | `test@example.com` | The recipient of the test email to send |

# Automatique Testing

This role is tested using Molecule against:
- Python 3.7, 3.8 and 3.9
- CentOS 7/8/9
- Debian 9/10/11