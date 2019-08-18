

INSTRUCTIONS INSTALLING JOLUPALABS CRUX REPO
=====
1. First download the necessary files:

   ```bash
   wget --no-ch https://raw.githubusercontent.com/jolupa/jolupalabs/master/jolupalabs.{httpup,pub}
   ```

2. Move the downloaded file to the proper folder:

   ```bash
   sudo mv jolupalabs.{httpup,pub} /etc/ports/
   ```

3. Add the ports line in yours */etc/prt-get.conf* to fetch the repo:

   prtdir /usr/ports/jolupalabs

4. Update the repo into your computer:

   ```bash
   sudo ports -u jolupalabs
   ```

NOTES
=====
1. All the builds have the locales installed, this is a **NOT** for the CRUX handbook. If you want to remove the locales just edit the *Pkgfile* and uncomment the *rm* line.

CONTACT
=====
If you have any question, doubt or problem regarding the ports, please feel free to contact me at jlpavon at me dot com or just open a [issue](https://github.com/jolupa/jolupalabs/issues)

XFCE INSTALLATION
=====
I provide two methods for installing the **Desktop Environment** Xfce.
1. Just make a depinst install of the meta package:

   ```bash
   sudo prt-get depinst xfce
   ```

2. Install the packages in this **same order**:

   ```bash
   sudo prt-get depinst xfce4-dev-tools libxfce4util xfconf libxfce4ui garcon exo xfce4-panel thunar thunar-volman xfce4-settings xfce4-session xfwm4 xfdesktop xfce4-appfinder tumbler xfce4-terminal xfce4-power-manager xfce4-notifyd xfce4-screenshooter mousepad xdg-user-dirs greybird-xfce elementary-xfce font-noto font-undefined-medium
   ```

3. Take a big cup of coffe or just relax...

4. To launch Xfce create a *.xinitrc* file in your *home* directory with the following content:
   ```bash
   #!/bin/sh
   exec ck-launch-session startxfce4
   ```

5. Enjoy this beatifull Desktop Manager!

OTHER PACKAGES IN THIS REPO
=====

You can find other packages not Xfce related in this repo, here's a list.

| PACKAGE NAME | VERSION | NOTES |
|---|:---:|---|
| Berry | 0.1.0 | |
| B43-fwcutter | 019 | |
| Broadcom-driver | 6.30.163.46 | |
| Claws-Mail GTK3 | GIT | The Git version with Gtk3 support |
| Colord | 1.3.5 | Added for Xfce4-settings color management support |
| Font Undefined Medium | 1.0 | |
| Granite | 5.2.4 | |
| Image Burner | 0.1.0 | |
| Lshw | B0.2.18 | List Computer Hardware |
| Libetpan | 1.9.3 | From [TimB87](https://github.com/TimB87/crux-ports) REPO to supply claws-mail-gtk3 dependency |
| Libgee | 0.20.1 | |
| Mbpfan | 2.1.1 | |
| Neofetch | 6.0.0 | |
| ObinslabStarter | 1.0.11 | Software for controlling the Anne Pro 2 Mechanical Keyboard. Right now it seems there's a segmentation fault error when you exit the program and the tray icon is still visible in the tray area, if you click it the segmentation fault occurs |
| Oneko | 1.2.sakura.5 | |
| Qogir Gtk theme | 2019-05-03 | Fantastic Flat Theme |
| Xiccd | 0.3.0 | Added for Xfce4-settings color management support |
 
