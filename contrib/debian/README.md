
Debian
====================
This directory contains files used to package halfyd/halfy-qt
for Debian-based Linux systems. If you compile halfyd/halfy-qt yourself, there are some useful files here.

## halfy: URI support ##


halfy-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install halfy-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your halfy-qt binary to `/usr/bin`
and the `../../share/pixmaps/halfy128.png` to `/usr/share/pixmaps`

halfy-qt.protocol (KDE)

