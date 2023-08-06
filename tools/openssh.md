# OpenSSH Cheat-Sheet

## Known Hosts

Remove Entry from the Known-Hosts File.
```bash
ssh-keygen -R hostname
```

## Using the SSH Config File
If you are regularly connecting to multiple remote systems over SSH, you can configure your remote servers with the `.ssh/config` file.

**Example:***
```ini
Host dev1
    HostName dev1.your-domain
    User ubuntu
    Port 2222
    IdentityFile ~/.ssh/targaryen.key

Host prod*
  User ubuntu

Host *
  ForwardAgent yes
  ForwardX11 yes
  ForwardX11Trusted yes
  ServerAliveInterval 60
  ServerAliveCountMax 10
```

Connect to a host (like *dev* , eg.) with `ssh dev`.
