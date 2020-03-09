

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
I don't know why the two ways to install Xfce the first one, the meta package, was installing the packages in the wrong way; so now I recommend this way.
1. Install the packages in this **same order**:

   ```bash
   sudo prt-get depinst libxfce4util xfconf libxfce4ui garcon exo xfce4-panel thunar thunar-volman xfce4-settings xfce4-session xfwm4 xfdesktop xfce4-appfinder tumbler xfce4-terminal xfce4-power-manager xfce4-notifyd xfce4-screenshooter mousepad xdg-user-dirs greybird-xfce elementary-xfce font-noto font-undefined-medium
   ```

3. Take a big cup of coffe or just relax...

4. To launch Xfce create a *.xinitrc* file in your *home* directory with the following content:
   ```bash
   #!/bin/sh
   exec ck-launch-session startxfce4
   ```

5. Enjoy this beatifull Desktop Environment!

XFCE DEPENDENCIES IN THIS REPOSITORY
=====

This are the dependencies you can find in this repository that are not avalaible in the oficila Crux repos.

| PACKAGE | DEPENDENCY | | |
|---|---|---|---|
| LibXfce4Ui | Libgtop | | |
| Thunar/Thunar-Volman | Gvfs | Udisks2 | |
| | | Gsettings-Desktop-Schemas | |
| | | Libatasmart | Ndctl |
| | | Libblockdev | |
| Xfce4-Settings | Colord | |

OTHER PACKAGES IN THIS REPO
=====

You can find other packages not Xfce related in this repo, here's a list.

| PACKAGE NAME | NOTES |
|---|:---:|
| Console Tdm | A Console Display Manager |
| Font Undefined Medium | |
| Font Noto | All the Noto Fonts in one package |
| Granite | |
| Image Burner | |
| Lshw | List Computer Hardware |
| Libgee | |
| Nordic | A beatiful Gtk3 theme based in nordic color scheme |
| ObinsKit | Software for controlling the Anne Pro 2 Mechanical Keyboard. |
| Qogir Gtk theme | Fantastic Flat Theme |
| Vala | Needed for Granite compilation |
