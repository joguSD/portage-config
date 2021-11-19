My portage configuration and install notes for use on future systems

# Installation

1) [Preparing disks](https://wiki.gentoo.org/wiki/Handbook:AMD64/Installation/Disks)
2) [Install stage3](https://wiki.gentoo.org/wiki/Handbook:AMD64/Installation/Stage)
3) [Enter chroot](https://wiki.gentoo.org/wiki/Handbook:AMD64/Installation/Base#Chrooting)
4) [Copy gentoo ebuild repo](https://wiki.gentoo.org/wiki/Handbook:AMD64/Installation/Base#Installing_a_Gentoo_ebuild_repository_snapshot_from_the_web)
5) Clone this configuration to `/etc/portage`.
6) Verify selected profile via `eselect profile list` is `default/linux/amd64/17.1/desktop/plasma/systemd (stable)`.
7) Update the world: `emerge --ask --verbose --update --deep --newuse @world`
8) Select all of the sets: `emerge --select @base @cli-tools @fonts @gui-apps @ime @kde`
9) [Set the timezone](https://wiki.gentoo.org/wiki/Handbook:AMD64/Installation/Base#Systemd)
10) [Configure locales](https://wiki.gentoo.org/wiki/Handbook:AMD64/Installation/Base#Configure_locales)
11) [Systemd `/etc/mtab`](https://wiki.gentoo.org/wiki/Systemd#/etc/mtab)
12) Set hostname in `/etc/hostname`
13) [Configure systemd networking](https://wiki.gentoo.org/wiki/Systemd#Network)
14) [Configure `/etc/fstab`](https://wiki.gentoo.org/wiki/Handbook:AMD64/Installation/System#Filesystem_information)
15) [Install bootloader](https://wiki.gentoo.org/wiki/Handbook:AMD64/Installation/Bootloader#Default:_GRUB2)
16) [Reboot](https://wiki.gentoo.org/wiki/Handbook:AMD64/Installation/Bootloader#Rebooting_the_system)
17) [Finalization, user creation, etc.](https://wiki.gentoo.org/wiki/Handbook:AMD64/Installation/Bootloader#Rebooting_the_system)
    * Groups: `wheel audio video users`
    * Enable base systemd services: `systemctl preset-all`
    * Enable `sddm`: `systemctl enable sddm.service`

To future me: I never tested this and it's from memory so some steps might be missing.
