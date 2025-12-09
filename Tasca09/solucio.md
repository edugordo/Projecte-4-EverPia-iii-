# T09 - Servidor NFS
## Projecte 4 - EverPia III
### Edu Gordo | SMX 2A

---

![imatge](IMG/1.png)

Creem els grups "devs" i "admins"

```
sudo groupadd devs
```
```
sudo groupadd admins
```
---

![imatge](IMG/2.png)

També creem un usuari per cada grup i li posem una contrasenya a cada usuari

```
sudo useradd -m -s /bin/bash -G devs dev01
```
```
sudo passwd dev01
```
```
sudo useradd -m -s /bin/bash -G admins admin01
```
```
sudo passwd admin01
```

---

![imatge](IMG/3.png)

info

```
sudo mkdir -p /srv/nfs/dev_projects
```
```
sudo mkdir -p /srv/nfs/admin_tools
```

---

![imatge](IMG/4.png)

info

```
sudo chown root:devs /srv/nfs/dev_projects
```
```
sudo chmod 770 /srv/nfs/dev_projects
```

---

![imatge](IMG/5.png)

info

```
sudo chown root:admins /srv/nfs/admin_tools
```
```
sudo chmod 770 /srv/nfs/admin_tools
```

---

![imatge](IMG/6.png)

info

```
sudo apt install nfs-kernel-server
```

---

![imatge](IMG/7.png)

info

```
sudo nano /etc/exports
```

`/srv/nfs/admin_tools 192.168.56.0/24(rw,sync)`

`/srv/nfs/dev_projects 192.168.56.0/24(rw,sync)`

---

![imatge](IMG/8.png)

info

```
sudo systemctl start nfs-kernel-server
```

```
sudo systemctl reload nfs-kernel-server
```

```
sudo exportfs -u
```

---

![imatge](IMG/9.png)

info

```
sudo rpcinfo -p 192.168.56.112
```

---

![imatge](IMG/10.png)

info

```
ping 192.168.56.112
```

---

![imatge](IMG/11.png)

info

```
sudo apt update
```

---

![imatge](IMG/12.png)

info

```
sudo apt install nfs-common -y
```

---

![imatge](IMG/13.png)

info

```
showmount - 192.168.56.112
```

---

![imatge](IMG/14.png)

info

```
sudo mkdir -p /mnt/dev_projects
```

```
sudo mkdir -p /mnt/admin_tools
```

---

![imatge](IMG/15.png)

info

```
sudo mkdir -p /mnt/admin_tools
```

```
sudo mount -t nfs 192.168.56.112:/srv/nfs/admin_tools /mnt/admin_tools
```

---

![imatge](IMG/16.png)

info

```
sudo touch /mnt/admin_tools/test01.txt
```

---

![imatge](IMG/17.png)

info

```
sudo ls -l /mnt/admin_tools
```

---

![imatge](IMG/18.png)

info

```
sudo exportfs -ra
```

```
sudo systemctl restart nfs-kernel-server
```

---

![imatge](IMG/19.png)

info

```
sudo mkdir -p /mnt/dev_projects
```

```
sudo mount -t nfs 192.168.56.112:/srv/nfs/dev_projects
```

---

![imatge](IMG/20.png)

info

---

![imatge](IMG/21.png)

info

---

![imatge](IMG/22.png)

info

```
sudo nano /etc/fstab
```
`192.168.56.112:/srv/nfs/admin_tools /mnt/admin_tools nfs default 0 0`

`192.168.56.112:/srv/nfs/dev_projects /mnt/dev_projects nfs default 0 0`

---

![imatge](IMG/23.png)

info

```
sudo reboot
```

---

![imatge](IMG/24.png)

info

```
mount | grep nfs
```

---
