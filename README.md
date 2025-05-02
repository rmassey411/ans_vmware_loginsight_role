ans_vmware_loginsight_role
=========

Install LogInsight client on server

Requirements
------------

- Linux
- Windows

Role Variables
--------------

| Variable            | Choices/Defaults    | Purpose/Description                                             |
| ------------------- | ------------------- | --------------------------------------------------------------- |
| installer_version   | N/A                 | determines which files are copied to server                     |
| installer_dir       | N/A                 | determines where files are copied to                            |
| loginsight_host         | N/A                 | fqdn of logging proxy                                           |
| N/A                 | N/A                 | N/A                                                             |
| N/A                 | N/A                 | N/A                                                             |


Dependencies
------------

N/A

VMware Info
------------
MSI:
- [Install doc](https://docs.vmware.com/en/vRealize-Log-Insight/8.10/com.vmware.log-insight.agent.admin.doc/GUID-E8A39702-6351-4ADB-949D-69667EF9161B.html)
- [Install agent](https://ci-data-collector-sandbox.s3.amazonaws.com/VMware-LI-Agent-8-10-0-20536336/VMware-Log-Insight-Agent-8.10.0-20536336.msi)
    ```
    msiexec.exe /i VMware-Log-Insight-Agent-8.10.0-20536336.msi /quiet SERVERHOST=loginsight.server.fqdn AUTOUPDATE=yes
    ```

RPM:
- [Install doc](https://docs.vmware.com/en/vRealize-Log-Insight/8.10/com.vmware.log-insight.agent.admin.doc/GUID-0F1114AB-0315-478C-B84B-863ABA393809.html)
- [Install agent](https://ci-data-collector-sandbox.s3.amazonaws.com/VMware-LI-Agent-8-10-0-20536336/VMware-Log-Insight-Agent-8.10.0-20536336.noarch.rpm)
    ```bash
    sudo SERVERHOST=loginsight.server.fqdn AUTOUPDATE=yes rpm -i VMware-Log-Insight-Agent-8.10.0-20536336.noarch.rpm
    ```

DEB:
- [Install doc](https://docs.vmware.com/en/vRealize-Log-Insight/8.10/com.vmware.log-insight.agent.admin.doc/GUID-8057DEC9-4EFB-4E5C-ADCF-E395B4DB0B71.html)
- [Install agent](https://ci-data-collector-sandbox.s3.amazonaws.com/VMware-LI-Agent-8-10-0-20536336/vmware-log-insight-agent_8.10.0-20536336_all.deb)
    ```bash
    sudo SERVERHOST=loginsight.server.fqdn AUTOUPDATE=yes dpkg -i vmware-log-insight-agent_8.10.0-20536336_all.deb
    ```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - ans_vmware_loginsight_role

License
-------
