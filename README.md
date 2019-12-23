# IaC-Heat-A

This is a Openstack Heat template to launch a flexible provisioned infrastructure. It was made for our Infrastructure as Code project, based on [this example by Erik Hjelmås](https://gitlab.com/erikhje/iac-heat-a).
The servers are initialized by [r10k](https://github.com/puppetlabs/r10k) using [this Puppet control repo](https://github.com/ErlendF/puppet-control-repo) (see lib/manager_boot.bash).

### Usage

Clone and launch in OpenStack with e.g.
```bash
# make sure you have security groups called default and linux
# edit iac_top_env.yaml and enter name of your keypair
git clone https://github.com/ErlendF/IaC-Heat.git
cd iac-heat-a
openstack stack create my_iac -t iac_top.yaml -e iac_top_env.yaml
```

### Authors
Aksel Baardsen, Johan Selnes, Erlend Fonnes

*During the project, we used [Vscode liveshare](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare), which is why Johan has all of our commits.*