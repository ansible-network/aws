# Provision initiator
The `cloud_vpn/deprovision_initiator` function will deprovision a VPN initiator
on AWS.
It is performed by calling the `cloud_vpn/deprovision_initiator` task from the role.
The task will process variables needed for deprovisioning a VM and call AWS Cloudformation.

Below is an example to deprovision a VPN initiator VM on AWS.

```
- hosts: localhost

  tasks:
    - name: Deprovision initiator
      include_role:
        name: ansible-network.aws
        tasks_from: cloud_vpn/deprovision_initiator
      vars:
        cloud_vpn_name: myvpn
```

## Notes
None
