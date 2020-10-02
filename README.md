

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

 4. Create the dir where the ports are contained:
    ```bash
    sudo mkdir /usr/ports/jolupalabs
    ```

4. Add the ports line in yours */etc/prt-get.conf* to fetch the repo:

   prtdir /usr/ports/jolupalabs

5. Update the repo into your computer:

   ```bash
   sudo ports -u jolupalabs
   ```

NOTES
=====
1. Enable the contrib repo because some dependencies reside there.

CONTACT
=====
If you have any question, doubt or problem regarding the ports, please feel free to contact me at jlpavon at me dot com or just open a [issue](https://github.com/jolupa/jolupalabs/issues)

XFCE INSTALLATION
=====
I don't know why the two ways to install Xfce the first one, the meta package, was installing the packages in the wrong way; so now I recommend this way.
1. To ensure you have a sane X installation I decided to put all the X dependencies with the first package you install from XFCE on **libxfce4util**
1. Install the packages in this **same order**:

   ```bash
   sudo prt-get depinst libxfce4util xfconf libxfce4ui garcon exo xfce4-panel thunar thunar-volman xfce4-settings xfce4-session xfwm4 xfdesktop xfce4-appfinder tumbler xfce4-terminal xfce4-power-manager xfce4-notifyd xfce4-screenshooter mousepad xdg-user-dirs
   ```

3. Take a big cup of coffe or just relax...

4. To launch Xfce create a *.xinitrc* file in your *home* directory with the following content:
   ```bash
   #!/bin/sh
   exec ck-launch-session startxfce4
   ```
   4.1 If you install tdm from this repo you can add this line inside ```bash .config/tdm/tdm/exit ``` following instructions from that REPO Readme.
   
5. If you have any problem launching XFCE and you have a an Intel graphic card, please try to use the mesa drivers in this repo.

6. Enjoy this beatifull Desktop Environment!
