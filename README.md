#Homelab Setup

## Initial setup
We're going to use an ubuntu laptop connected to an isolated network to boot strap machines also connect to that network.  The laptop will be referred to as 'bootstrap machine' or just 'bootstrap' henceforth.  The laptop's name is "thinkpad" and that is set in host_vars and inventory.  Change that if you need to

### Bootstrap Prereqs

1.  Install docker and ansible.
```
sudo apt install docker.io ansible -y
```

2.  Download the centos7 minimal iso and set as the variable centos_iso in hostvars/thinkpad.yaml
https://ubuntu.com/download/server

3.  Copy the ubuntu 7 ISO contents to a place where ansible will be able to easily find it
```
sudo mkdir /var/opt/isos
sudo mv [DOWNLOAD DIR]/[CENTOS ISO] /var/opt/isos
```


