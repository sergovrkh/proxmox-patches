# proxmox-patches

pveproxy patches

Added the ability to assign a specific ip address for pveproxy instead of the standard 0.0.0.0

How to apply?

git clone https://github.com/sergovrkh/proxmox-patches.git

cd proxmox-patches/pveproxy

patch -d/ -p0 < pveproxy.patch 

Configuring

Create file /etc/default/pveproxy (if does not exist)

Add BIND_ADDR='your IP'

Restart pveproxy

pveproxy stop && pveproxy start

Rollback

cd proxmox-patches/pveproxy

patch -R -d/ -p0 < pveproxy.patch

Author

Sergey Vertiporokh

