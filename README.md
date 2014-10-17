# pfSense firewall ansible playbook

Ansible playbook to automate some pfSense firewall tasks, all tasks will be excecuted by using roles.


## Current automated tasks

* Install python into pfSense firewalls
* Patch old pfSense release againts POODLE vulnerability, disabling SSLv3 support in lighttpd

## Excecute playbook

Excecute the playbook using the following command:

```bash
ansible-playbook -i hosts site.yml
```

The above command will execute all tasks, if you already have python installed in you firewall you can execute the poodle path task by execute:

```bash
ansible-playbook -i hosts --tags "sslv3" site.yml
```
