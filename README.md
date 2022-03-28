# Run Linux and Windows updates with Ansible

## Requirements
- Ansible 2.9

&nbsp;

## Workflow
```mermaid
graph TD;
    CLEAN_REPORT_FILES-->id1((WINDOWS));
    CLEAN_REPORT_FILES-->id2((LINUX));
    id2((LINUX))-->CHECK-->UPDATE-->REBOOT;
    id1((WINDOWS))-->WIN_CHECK-->PRE_REBOOT-->WIN_UPDATE-->POST_REBOOT;
    POST_REBOOT-->HTML_REPORTING;
    REBOOT-->HTML_REPORTING;
```

&nbsp;
  
## Setup
1. Complete inventory with your own hosts
2. Configure hosts access with SSH or WINRM (see groups_vars folder)
3. Manage secrets and protect all sensitive data with ansible vault (optional)
4. Run :
```bash
ansible-playbook main.yml -i inventory
```

&nbsp;
  
### Reporting

  ![alt text](https://github.com/kenybapin/ansible-sys-updates/blob/main/misc/report.jpg?raw=true)
