INSTALLING CRUX
=====
Some notes for my use about installing CRUX (3.5) in my current laptop (MacBook White Mid 2009)

BEAR IN MIND
=====
1. Download ISO from [CRUX Website](https://crux.nu/Main/Download)
2. Also I need the Wifi driver:
   FWCutter -> I made a port for installing the fwcutter needed by the driver and the broadcom-wl driver. Both packages are in [jolupalabs ports](https://github.com/jolupa/jolupalabs)

INSTALLATION
=====

The installatiion is very straigth forward and following the handbook in the [CRUX Website](https://crux.nu/Main/Handbook3-5) is the most I have to do.
The kernel conf. with the .config shipped on the ISO is enough to make the hardware functioning the only things I have to tweak are (*keep this update with some notes)*:

1. Enable **DRI** and activate **Nouveau** for the Nvidia graphics card (I don't use the propietary drivers)
2. Activate **AppleSMC** in the drivers section.

I *think* that's all in the kernel config to make it working with the mac.

*Note* To activate the Touchpad if anyday I want to use it I have to enable the **XF86Drivers -> Appletouchpad**

POST INSTALLATION
=====

After rebooting with the linux kernel installed.

1. Enable my REPO with the instructions on the site [jolupalabs](https://github.com/jolupa/jolupalabs) and after activating it the ```prt-get depinst broadcom-driver``` this will install the packages required.
2. Follow instructions to create a user for pkg treatment, very handy, from [here](https://crux.nu/Wiki/PostInstallationNotes)
3. Install all the Xfce DE and all it's dependencies with ```prt-get depinst xfce```
4. Important to take care of [this](https://crux.nu/Wiki/TroubleshootingXKB) if X won't start.
