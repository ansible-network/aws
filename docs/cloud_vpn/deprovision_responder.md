# Deprovision responder
The `cloud_vpn/deprovision_responder` function will deprovision a VPN responder
on AWS.
It is performed by calling the `cloud_vpn/deprovision_responder` task from the role.
The task will process variables needed for deprovisioning a VM and call AWS Cloudformation.

Below is an example to deprovision a VPN responder VM on AWS.

```
- hosts: localhost

  tasks:
    - name: Deprovision responder
      include_role:
        name: ansible-network.aws
        tasks_from: cloud_vpn/deprovision_responder
      vars:
        cloud_vpn_name: myvpn
```

## Notes
None
