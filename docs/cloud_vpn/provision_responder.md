# Provision responder
The `cloud_vpn/provision_responder` function will provision a VPN responder
on AWS.
It is performed by calling the `cloud_vpn/provision_responder` task from the role.
The task will process variables needed for provisioning a VM and call AWS Cloudformation.

Below is an example to provision a VM that will be the responder of the VPN with AWS.

```
- hosts: localhost

  tasks:
    - name: Provision responder
      include_role:
        name: ansible-network.aws
        tasks_from: cloud_vpn/provision_responder
      vars:
        cloud_vpn_name: myvpn
        cloud_vpn_responder_vpc_cidr: 10.0.0.0/16
        cloud_vpn_responder_cidr: 10.0.0.0/24
        cloud_vpn_responder_private_ip: 10.0.0.10
        cloud_vpn_responder_key_name: mykey
        cloud_vpn_responder_instance_size: t2.micro
        cloud_vpn_responder_image_id: ami-2948371230984
```

## Notes
None
