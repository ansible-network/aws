# aws

This Ansible Network role provides a set of platform dependent functions that
are designed to work with AWS.

## Requirements

* Ansible 2.7 or later
* Ansible Network Engine Role 2.7.0 or later

## Functions

This section provides a list of the availabe functions that are included
in this role.  Any of the provided functions can be implemented in Ansible
playbooks to perform automation activities on AWS.

Please see the documentation link for each function for details on how to use
the function in an Ansible playbook.

### Cloud VPN
* cloud_vpn/configure_vpn_responder [[source]](https://github.com/ansible-network/aws/blob/devel/tasks/cloud_vpn/configure_vpn_responder.yaml) [[docs]](https://github.com/ansible-network/aws/blob/devel/docs/cloud_vpn/configure_vpn_responder.md)
* cloud_vpn/provision_initiator [[source]](https://github.com/ansible-network/aws/blob/devel/tasks/cloud_vpn/provision_initiator.yaml) [[docs]](https://github.com/ansible-network/aws/blob/devel/docs/cloud_vpn/provision_initiator.md)
* cloud_vpn/deprovision_initiator [[source]](https://github.com/ansible-network/aws/blob/devel/tasks/cloud_vpn/deprovision_initiator.yaml) [[docs]](https://github.com/ansible-network/aws/blob/devel/docs/cloud_vpn/deprovision_initiator.md)
* cloud_vpn/provision_responder [[source]](https://github.com/ansible-network/aws/blob/devel/tasks/cloud_vpn/provision_responder.yaml) [[docs]](https://github.com/ansible-network/aws/blob/devel/docs/cloud_vpn/provision_responder.md)
* cloud_vpn/deprovision_responder [[source]](https://github.com/ansible-network/aws/blob/devel/tasks/cloud_vpn/deprovision_responder.yaml) [[docs]](https://github.com/ansible-network/aws/blob/devel/docs/cloud_vpn/deprovision_responder.md)

## License

GPLv3

## Author Information

Ansible Network Community
