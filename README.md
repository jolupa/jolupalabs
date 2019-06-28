INSTRUCTIONS INSTALLING JOLUPALABS CRUX REPO
=====
1. First download the necessary files:

   ```$wget --no-ch https://raw.githubusercontent.com/jolupa/jolupalabs/master/jolupalabs.{httpup,pub}```

2. Move the downloaded file to the proper folder:

   ```$sudo mv jolupalabs.{httpup,pub} /etc/ports/```

3. Add the ports line in yours */etc/prt-get.conf* to fetch the repo:

   prtdir /usr/ports/jolupalabs

4. Update the repo into your computer:

   ```$sudo ports -u jolupalabs```

NOTES
=====
1. All the builds have the locales installed, this is a **NOT** for the CRUX handbook. If you want to remove the locales just edit the *Pkgfile* and uncomment the *rm* line.

CONTACT
=====
If you have any question, doubt or problem regarding the ports, please feel free to contact me at jlpavon at me dot com

XFCE INSTALLATION
=====
I provide two methods for installing the **Desktop Environment** Xfce.
1. Just make a depinst install of the meta package:

   ```$sudo prt-get depinst xfce```

2. Install the packages in this **same order**:

   ```$sudo prt-get depinst xfce4-dev-tools libxfce4util xfconf libxfce4ui garcon exo xfce4-panel thunar thunar-volman xfce4-settings xfce4-session xfwm4 xfdesktop xfce4-appfinder tumbler xfce4-terminal xfce4-power-manager xfce4-notifyd xfce4-screenshooter mousepad xdg-user-dirs greybird-xfce elementary-xfce font-noto font-undefined-medium```

3. Take a big cup of coffe or just relax...

4. To launch Xfce create a *.xinitrc* file with the following content:
   ```#!/bin/sh
   exec ck-launch-session startxfce4```

5. Enjoy this beatifull Desktop Manager!
