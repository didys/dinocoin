
Debian
====================
This directory contains files used to package dinocoind/dinocoin-qt
for Debian-based Linux systems. If you compile dinocoind/dinocoin-qt yourself, there are some useful files here.

## dinocoin: URI support ##


dinocoin-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install dinocoin-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your dinocoinqt binary to `/usr/bin`
and the `../../share/pixmaps/dinocoin128.png` to `/usr/share/pixmaps`

dinocoin-qt.protocol (KDE)

