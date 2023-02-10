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
add this to the end of /etc/fstab

```
/var/lib/nix /nix none bind 0 0
```

exit the transactional-update shell

set selinux to permissive by edditing the config

```bash
sudo nano /etc/selinux/config
```

reboot

Install nix

```bash
sh <(curl -L https://nixos.org/nix/install) --daemon
```
