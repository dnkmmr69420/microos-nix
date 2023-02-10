# microos-nix
Guide to install nix package manager on microos

Enter the transactional update shell

```bash
sudo transactional-update shell
```

Create a /nix subvolume in the transactional-update shell

```bash
mksubvolume /nix
```

create /var/lib/nix

```bash
mkdir /lib/var/nix
```

add this to the end of /etc/fstab

```
/var/lib/nix /nix none bind 0 0
```

edit /etc/selinux/config and set it to permissive


```
SELINUX=permissive
```

exit the transactional-update shell


reboot

Install nix

```bash
sh <(curl -L https://nixos.org/nix/install) --daemon
```

until I figure out how to permenatly disable selinux on microos, you will have to do the following on every boot

```bash
sudo setenforce permissive
```
```bash
sudo systemctl enable --now nix-daemon.socket
```
