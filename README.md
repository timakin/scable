Dsync[WIP]
====

- install rsync. openssl, openssl-devel, and openssl-server to the container.
- install rsync lsyncd lua to the local host.
- `useradd` to open a channel on the container and insert a line that define `rsync` user group as `su`.
    - check whether `rsync` user group exists.
    - check whether `rsync` user group is set as a super user on `/etc/sudoers`
- generate a ssh-key pair, change mode of it, and save it to ~/.ssh.
- add pub_key to container's `~/.ssh/authorized_keys`.
- add `lsyncd.conf` to the local host and launch `lsyncd`