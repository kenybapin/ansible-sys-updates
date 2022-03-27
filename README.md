# Linux and Windows updates with Ansible

## Requirements
- ansible 2.9
- complete inventory file with hosts windows (keep windows and linux groups).
- configure hosts access : SSH / WINRM with privileged accounts (see vars in groups_vars folder)
- if necessary, manage secrets and protect all sensitive data with ansible vault.

&nbsp;

## Workflow

<screenshot>

&nbsp;
  
## Setup
```bash
ansible-playbook main.yml -i inventory
```

&nbsp;
  
### Reporting
