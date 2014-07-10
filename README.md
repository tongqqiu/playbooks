

# GCE Example

### Configuration

```
gce_inventory/gce.ini
host_vars/gce_vars.yml
```

### Provision

```
sudo ansible-playbook -i gce_inventory/dev-inventory.ini gce-web-provision.yml -f 5 -vv
```
Need to include an unrelated inventory file if GCE cloud doesn't contain any instances. Otherwise
````
ERROR: provided hosts list is empty
````

### Deploy

```
sudo ansible-playbook -i gce_inventory/. gce-web.yml -f 5 -vv
```

### Destory

```
sudo ansible-playbook -i gce_inventory/. gce-web-destory.yml -f 5 -vv
```
