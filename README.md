# ansible-tower-credential-types

Playbooks that will create some commonly-needed Credential Types in Ansible Tower that don't come with the default install.

Designed for and tested under Ansible Tower 3.8.3.

Currently available:

* ServiceNow (for use with `servicenow.itsm` collection)
* F5 (for use with `f5networks.f5_modules` collection)

# How to use

Set Tower information via environment variables `TOWER_HOST`, `TOWER_USERNAME`, `TOWER_PASSWORD`, and `TOWER_VERIFY_SSL`. This can be done from within Tower by using the built-in Ansible Tower credential type, or on the CLI using exports:
```
export TOWER_HOST=my-tower-host
export TOWER_USERNAME=admin
export TOWER_PASSWORD=password
export TOWER_VERIFY_SSL=no
```

Then run the playbook against either `localhost`, or an inventory contianing your Tower endpoint.
