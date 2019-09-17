# IaC-Heat-A

This is a Heat template to launch a flexible provisioned infrastructure. The servers are initialized based on [this Puppet control repo](https://gitlab.com/erikhje/control-repo-a).

Clone and launch in OpenStack with e.g.
```bash
# make sure you have security groups called default and linux
# edit iac_top_env.yaml and enter name of your keypair
git clone https://gitlab.com/erikhje/iac-heat-a.git
cd iac-heat-a
openstack stack create my_iac -t iac_top.yaml -e iac_top_env.yaml
```

