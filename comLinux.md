# Linux

## Learn

[Linux server monitoring commands](https://www.hpe.com/us/en/insights/articles/16-linux-server-monitoring-commands-you-really-need-to-know-1703.html)
[Linux Users and Groups](https://www.linode.com/docs/tools-reference/linux-users-and-groups/)
[Guide to useradd](https://www.tecmint.com/add-users-in-linux/)
[Linux Directory Structure and Important Files Paths Explained](https://www.tecmint.com/linux-directory-structure-and-important-files-paths-explained/)
[Memory usage](https://www.binarytides.com/linux-command-check-memory-usage/)
[Boot to CLI](https://askubuntu.com/questions/52089/how-do-i-boot-to-a-command-line-interface-instead-of-a-gui)
[start Ubuntu CLI](https://askubuntu.com/questions/859630/how-to-start-ubuntu-in-console-mode)
[start lightdm services](https://askubuntu.com/questions/624816/how-to-start-lightdm-services-at-startup)
[GDM vs LightDM](https://itsfoss.com/switch-gdm-and-lightdm-in-ubuntu-14-04/)
[Disk Usage](https://www.cyberciti.biz/faq/linux-check-disk-space-command/)
[Ubuntu Server GUIs](https://thishosting.rocks/ubuntu-server-guis/)
[Florian N / pydash](https://gitlab.com/k3oni/pydash)
Learn **Sleep**
[Ubuntu Server Sleep](https://unix.stackexchange.com/questions/25133/ubuntu-server-continuously-goes-to-sleep/25151#25151)
[Disable sleep](https://askubuntu.com/questions/47311/how-do-i-disable-my-system-from-going-to-sleep)
[WakeOnLan](https://help.ubuntu.com/community/WakeOnLan)

## Install

### Network

- View network config: `sudo ifconfig`
**Network** Setup
- Edit file _etc_network/interfaces
- change **last line** ‘iface default inet dhcp’ to
- find network card name `ifconfig`
- copy file `cp /etc/network/interfaces /etc/network/interfaces.old`
- edit file `sudo vim /etc/network/interfaces`
- setup new ip: `sudo ifup [network card name]`

``` bash
Wifi
iface default inet static
address 192.168.1.123
netmask 255.255.255.0
network 192.168.1.1
gateway 192.168.1.1

Ethernet
auto lo
iface lo inet loopback
iface eth0 inet static
address 192.168.1.99
netmask 255.255.255.0
gateway 192.168.1.1
```

### VNC

- [Headless VM Server Using KVM](https://www.ostechnix.com/setup-headless-virtualization-server-using-kvm-ubuntu/)
- [Install and Configure VNC](https://linuxize.com/post/how-to-install-and-configure-vnc-on-ubuntu-18-04/)
- [Setup VNC Server on Ubuntu](https://www.smarthomebeginner.com/setup-vnc-server-on-ubuntu-linux/)

- [NUC8 Ethernet Adapter](https://downloadcenter.intel.com/download/22283/Intel-Ethernet-Adapter-Complete-Driver-Pack)
- [Ubuntu Server GUIs](https://thishosting.rocks/ubuntu-server-guis/)
- [Webmin](https://thishosting.rocks/how-to-install-webmin-on-ubuntu-16-04/)

```bash
sudo apt-get install xfce4 xfce4-goodies
sudo apt-get install tightvncserver
vncserver
view processes: ps -ef | grep Xtightvnc
kill: vncserver -kill :1 (process number)
cp ~/.vnc/xstartup ~/.vnc/xstartup_backup
vim ~/.vnc/xstartup
```

Network inteface nmcli
Change File to:

``` bash
#!/bin/sh
def
export XKL_XMODMAP_DISABLE=1
unset SESSION_MANAGER
unset DBUS_SESSION_BUS_ADDRESS

xrdb $HOME/.Xresources
xsetroot -solid grey

startxfce4 &
```

To Login - run vncserver
To login (With vnc client) - goto 192.168.1.111:5901
when done: `vncserver -kill :1` (process number 1)

### Disks

- [Resize LVM Partition](https://www.looklinux.com/resize-lvm-how-to-increase-an-lvm-partition/)
- [Extend/Reduce LVM](https://www.tecmint.com/extend-and-reduce-lvms-in-linux/)
- [Logical Volume Manager](https://www.landoflinux.com/linux_lvm_command_examples.html)
- [Resize partitions](https://askubuntu.com/questions/390769/how-do-i-resize-partitions-using-command-line-without-using-a-gui-on-a-server)
- [Delete LVM volume](https://www.thegeekdiary.com/centos-rhel-how-to-delete-lvm-volume/)
- [new disk to a volume group](http://computers-it.com/linux/linux_add_new_disk_to_VG.php)
- [fdisk Commands to Manage Partitions](https://www.tecmint.com/fdisk-commands-to-manage-linux-disk-partitions/)
- [Basic Guide To Encrypting Linux Partitions With LUKS - LinuxConfig.org](https://linuxconfig.org/basic-guide-to-encrypting-linux-partitions-with-luks)

#### Encrypted

- Display disks in Tree: `lsblk`
- Install: `sudo apt get install cryptsetup`
- Mount Drives: `sudo mount /dev/sdb1 /media/username/element`
- UnMount Drives: `sudo umount /media/username/element`
- Delete partition: `sudo fdisk d /dev/sdc1`
- Encrypt Disk: `sudo cryptsetup luksFormat /dev/sdb1`
- Format ext4: `sudo mkfs.ext4 /dev/mapper/element`
- unmount drive `sudo umount -f /media/backupBW`
- check for busy processes: `lsof | grep '/media/backupBW'`
- kill process `kill` or `kill -9`
- close luks: `sudo cryptsetup close backupBW`
- open lukes drive `sudo cryptsetup --type luks open /dev/sdc1 backupBW`
- mount drive `sudo mount -t ext4 /dev/mapper/backupBW /media/backupBW`
- own folder `sudo chown username /media/backupBW`

**Mount** drive

```bash
sudo cryptsetup --type luks open /dev/sdb1 encrypted
sudo mount -t ext4 /dev/mapper/element /media/element
sudo chown username /media/element
chown -R username:group /mountpoint
```

**Unmount** drive

```bash
sudo umount -l /media/element
sudo -l lazy   -f force
sudo cryptsetup close element
```

**Reboot** Commands

```bash
sudo cryptsetup open /dev/nvme0n1p3 evo
sudo mount -t ext4 /dev/mapper/evo /media/evo
sudo cryptsetup open /dev/sda1 ssd
sudo mount -t ext4 /dev/mapper/ssd /media/ssd
sudo cryptsetup open /dev/sdb1 element
sudo mount -t ext4 /dev/mapper/element /media/element
sudo chown username /media/ssd
sudo chown username /media/evo
sudo chown username /media/element
reload file `source ~/.zshrc`
```

### KVM

Check ubuntu version" `lsb_release -d`
Install The **Packages**
Install KVM with packages: `sudo apt install qemu-kvm libvirt-clients libvirt-daemon-system bridge-utils virt-manager`
sudo apt-get install qemu-kvm libvirt-bin bridge-utils virt-manager
sudo adduser "name" libvirtd

### Xu4

[Headless setup](https://wiki.odroid.com/odroid-xu4/application_note/software/headless_setup)

```bash
sudo apt update
sudo apt install x11vnc
Run VNC server
x11vnc -display :0 -auth guess
```

### Debian Raspbian

- Config `sudo raspi-config`
- Set auto login (Don't need)
  - edit _etc_inittab
  - Change line: `1:2345:respawn:/sbin/getty --noclear 38400 tty1`
  - To (basically ad ‘–autologin ‘username’’ before –noclear)
  - To `1:2345:respawn:/sbin/getty --autologin pi --noclear 38400 tty1`
- Change Password: `passwd`
- Change username
  - Enable root: `sudo passwd root`
  - Login as root
  - Change name: `usermod -l myuname pi`
  - Change folder: `usermod -m -d /home/myuname myuname`
  - Disable root: `sudo passwd -l root`
- Don't install ftp, use sftp, part of ssh: `sftp Username@address`
- VNC server part of config now
- ssh: `ssh pi@192.168.1.123` password: `raspberry`
- config `sudo raspi-config`
- Run GUI: `startx`
- shutdown: `sudo shutdown -r now`

## Linux CLI

- Linux CommandsStart Desktop: startx Graphical version of sudo: gksodu graphical text editor: leafpad Get Software files from Internet: sudo apt-get
