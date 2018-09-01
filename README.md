# Installing-gimp-plugin-registry-into-Gimp-2.10


### To easily download around 100 plugins on Linux install the 'gimp-plugin-registry' 

* 1) First ensure plug-in folder exists. If you already have 2.8 install it will exist but just to make sure
$ mkdir -p /usr/lib/gimp/2.0/plug-ins


* 2) Install the 'gimp-plugin-registry'for Debian/Ubuntu this is
$ sudo apt install gimp-plugin-registry

This installs a bunch (100 ish) plugins into usr/lib/gimp/2.0/plug-ins

* 3)  copy the plugin scripts to the 2.10 folder 

If you've installed via Flatpak GIMP install
$ cp -r /usr/lib/gimp/2.0/plug-ins ~/.var/app/org.gimp.GIMP/config/GIMP/2.10

If you've installed via Snap GIMP Install
$ cp -r /usr/lib/gimp/2.0/plug-ins ~/snap/gimp/47/.config/GIMP/2.10


### TL;DR
$ mkdir -p /usr/lib/gimp/2.0/plug-ins
$ sudo apt install gimp-plugin-registry
$ cp -r /usr/lib/gimp/2.0/plug-ins ~/.var/app/org.gimp.GIMP/config/GIMP/2.10  
OR
$ cp -r /usr/lib/gimp/2.0/plug-ins ~/snap/gimp/47/.config/GIMP/2.10


** Note: If you haven't already installed Gimp 2.10 I recommend Flatpak or Snaps as modern developer orientated distribution systems

* Flatpak
To check if Flatpak installed
$ flatpak --version

To [install Flatpak](https://flatpak.org/setup/)

And to install Gimp 2.10
$ flatpak install https://flathub.org/repo/appstream/org.gimp.GIMP.flatpakref

To update ALL your flatpak's   
$ flatpak update

* Snap
To check if Snap already installed (default in Ubuntu)
$ snap --version

If not, then install via
$ sudo apt install snapd

Then to install Gimp 2.10
$ sudo snap install gimp

To refresh ALL your snaps 
$ snap refresh
