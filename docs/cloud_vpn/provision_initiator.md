# Provision initiator
The `cloud_vpn/provision_initiator` function will provision a VPN initiator
on AWS.
It is performed by calling the `cloud_vpn/provision_initiator` task from the role.
The task will process variables needed for provisioning a VM and call AWS Cloudformation.

Below is an example to provision a VM that will be the initiator of the VPN with AWS.

```
- hosts: localhost

  tasks:
    - name: Provision initiator
      include_role:
        name: ansible-network.aws
        tasks_from: cloud_vpn/provision_initiator
      vars:
        cloud_vpn_name: myvpn
        cloud_vpn_initiator_provisioner: aws
        cloud_vpn_initiator_vpc_cidr: 10.0.0.0/16
        cloud_vpn_initiator_cidr: 10.0.0.0/24
        cloud_vpn_initiator_private_ip: 10.0.0.10
        cloud_vpn_initiator_key_name: mykey
        cloud_vpn_initiator_instance_size: t2.micro
        cloud_vpn_initiator_image_id: ami-2948371230984
```

## Notes
None
