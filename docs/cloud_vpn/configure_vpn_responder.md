# Configure VPN as responder
The `cloud_vpn/configure_vpn_responder` function will configure IPSEC VPN as responder
on AWS VPN.
It is performed by calling the `cloud_vpn/configure_vpn_responder` task from the role.
The task will process variables needed for VPN configuration and apply it to the device.

Below is an example to configure an IPSEC VPN as responder on AWS VPN, where
the initiator is VyOS device:

```
- hosts: localhost

  tasks:
    - name: Configure IPSEC VPN as responder
      include_role:
        name: ansible-network.aws
        tasks_from: cloud_vpn/configure_vpn_responder
      vars:
        cloud_vpn_name: myvpn
        cloud_vpn_psk: mypsksecret
        cloud_vpn_tunnel_cidr: 169.254.56.24/30
        cloud_vpn_tunnel_failover_cidr: 169.254.56.24/30
        cloud_vpn_responder_provider: aws_vpn
        cloud_vpn_responder_vpc_id: vpc-0321494
        cloud_vpn_responder_route_table_id: rtb-934562
        cloud_vpn_initiator_provider: vyos
        cloud_vpn_initiator_public_ip: 18.191.132.220
        cloud_vpn_initiator_cidr: 10.0.0.0/24
        cloud_vpn_initiator_bgp_asn: 65000
```

## Notes
None
