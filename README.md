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
