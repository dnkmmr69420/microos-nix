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

exit the transactional-update shell

```bash
exit
```

reboot the system

```bash
systemctl reboot
```

make /var/lib/nix directory

```bash
sudo mkdir /var/lib/nix
```
mount /var/lib/nix on /nix

```bash
sudo mount --bind /var/lib/nix /nix
```
