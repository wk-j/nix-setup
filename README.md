## Setup Nix

### Install

```
curl https://nixos.org/nix/install | sh
```

### Uninstall

1. Delete /Library/LaunchDaemons/org.nixos.nix-daemon.plist

```
  sudo launchctl unload /Library/LaunchDaemons/org.nixos.nix-daemon.plist
  sudo rm /Library/LaunchDaemons/org.nixos.nix-daemon.plist
```

2. Restore /etc/bashrc.backup-before-nix back to /etc/bashrc

```
  sudo mv /etc/bashrc.backup-before-nix /etc/bashrc
```

(after this one, you may need to re-open any terminals that were
opened while it existed.)

3. Restore /etc/zshrc.backup-before-nix back to /etc/zshrc

```
  sudo mv /etc/zshrc.backup-before-nix /etc/zshrc
```

(after this one, you may need to re-open any terminals that were
opened while it existed.)

4. Delete the files Nix added to your system:

```
  sudo rm -rf /etc/nix /nix /var/root/.nix-profile /var/root/.nix-defexpr /var/root/.nix-channels /Users/wk/.nix-profile /Users/wk/.nix-defexpr /Users/wk/.nix-channels
  ```

and that is it.