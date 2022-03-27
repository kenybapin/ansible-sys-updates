# Run Linux and Windows updates with Ansible

## Requirements
- Ansible 2.9
- Complete inventory file with hosts windows (keep windows and linux groups).
- Configure hosts access : SSH / WINRM with privileged accounts (see vars in groups_vars folder)
- Manage secrets and protect all sensitive data with ansible vault (if necessary)

&nbsp;

## Workflow
```mermaid
graph TD;
    CLEAN_FILES-->id1((WINDOWS));
    CLEAN_FILES-->id2((LINUX));
    id2((LINUX))-->CHECK-->UPDATE-->REBOOT;
    id1((WINDOWS))-->WIN_CHECK-->PRE_REBOOT-->WIN_UPDATE-->POST_REBOOT;
    POST_REBOOT-->REPORTING;
    REBOOT-->REPORTING;
```

&nbsp;
  
## Setup
```bash
ansible-playbook main.yml -i inventory
```

&nbsp;
  
### Reporting

  ![alt text](https://github.com/kenybapin/ansible-sys-updates/blob/main/misc/report.jpg?raw=true)
