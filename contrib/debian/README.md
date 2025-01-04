
Debian
====================
This directory contains files used to package egamingcoind/egamingcoin-qt
for Debian-based Linux systems. If you compile egamingcoind/egamingcoin-qt yourself, there are some useful files here.

## egamingcoin: URI support ##


egamingcoin-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install egamingcoin-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your egamingcoin-qt binary to `/usr/bin`
and the `../../share/pixmaps/egamingcoin128.png` to `/usr/share/pixmaps`

egamingcoin-qt.protocol (KDE)

