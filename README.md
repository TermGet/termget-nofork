﻿# What is TermGet?
TermGet is a project made by PizzaLovingNerd, several others.

TermGet is a frontend for:

 - apt-get
 - xbps
 - dnf
 - eopkg
 - zypper
 - pacman
 - yaourt
 - homebrew
 - apm
 - pkg
 - chromebrew
 - emerge
 - pip
 - sol  (Coming Soon)
 - chocolatey (Coming Soon)


## What are some of it's features

 - Simple, easy to use interface
 - Works in the command line
 - Supports a lot of package managers
 - Feature rich
 - Works on any Linux/Mac distribution (and soon Windows)
 - Great for introducing package management to new users
 - Code is easy to modify.

## Where can I get TermGet?

To get an alpha build, please clone the [TermGet GitHub repository](https://github.com/PizzaLovingNerd/TermGet)

To get a beta or release build, please go to the releases tab, of the [TermGet GitHub repository](https://github.com/PizzaLovingNerd/TermGet/releases)

## How do I install TermGet on Linux, and BSD

First install python3. Once you've done that, download and unzip TermGet. Now open a terminal, and go to your downloads folder (Or where ever you have unzipped it).

If this is a first time install or your upgrading TermGet, type:
    bash install.sh

## First Time Setup On Linux, and BSD

After installing, run TermGet using

    termget

you should get a message that sort of looks like this:

    Please choose a package manager

    1. apt-get (For Debian, and Debian based systems.)
    2. xbps (For Void Linux, and Void Linux based systems)
    3. dnf (For Fedora, and Fedora based systems)
    4. zypper (For OpenSUSE, and OpenSUSE based systems)
    5. eopkg (For Solus, and Solus based systems)
    6. pacman (For Arch, and Arch based systems)
    .....list goes on

Choose your distribution's package manager using the number. My package manager is eopkg, so I would type "5" and press enter.

## How do I install TermGet on ChromeOS
### Warning: Not fully tested

First put your Chromebook in [developer mode](https://www.howtogeek.com/210817/how-to-enable-developer-mode-on-your-chromebook/ "developer mode").

Check if Python3 is already installed on your system. Do so by typing

    python3

If you are brought to a prompt, then it is installed, you may now type exit() to leave Python3

If not, then [watch this video](https://www.youtube.com/watch?v=X7Y8b2S3nEA)

If you would rather read instead of a video, [click here](https://wsvincent.com/install-python3-chromebook/)

Now download Termget and cd into it, then run

    bash install.sh

and it will install, if you get errors report it to the github issues.

That's it, type "termget" into the prompt and you should be good

## First Time Setup On macOS

After installing, run TermGet using

    termget

you should get a message that sort of looks like this:

    Please choose a package manager

    1. apt-get (For Debian, and Debian based systems.)
    2. xbps (For Void Linux, and Void Linux based systems)
    3. dnf (For Fedora, and Fedora based systems)
    4. zypper (For OpenSUSE, and OpenSUSE based systems)
    5. eopkg (For Solus, and Solus based systems)
    6. pacman (For Arch, and Arch based systems)
    .....list goes on

Choose homebrew by typing "11".
## How do I use TermGet on Linux, BSD, or Mac

This section gets updated with every release, if you are using an alpha or beta build, there might be extra features that aren't on this section of the README file.

TermGet is really easy to use. To run it, all you have to do is open a terminal, and type:

    sudo termget


Just select using the number (for example if my package manager was apt-get, I would type the number 1, and press enter).

Once your package manager has been chosen, you will get a message like this:

    Please choose an action

    1. Search for packages
    2. Install an application
    3. Remove an application
    4. Update all packages
    5. Update Database
    6. Clean
    7. Credits
    8. Exit

*We will be using "eopkg" in the examples below.*
*Results may vary for other package managers*

### Searching for Packages

Search searches for packages. This is what it looks like when I search Minetest:

    Please enter search query: minetest

    minetest         - Minetest, an open source infinite-world block sandbox game with survival and crafting.
    minetest-dbginfo - Debug symbols for minetest

    Press enter to continue

### Installing a package

Installing a package downloads and installs a package. This is what it looks like if I install Minetest:

    Total size of package(s): 6.73 MB
    Downloading 1 / 1
    Package minetest found in repository Solus
    minetest-0.4.16-4-1-x86_64.eopkg [cached]
    Installing 1 / 1
    minetest-0.4.16-4-1-x86_64.eopkg [cached]
    Installing minetest, version 0.4.16, release 4
    Extracting the files of minetest
    Installed minetest
	    [✓] Syncing filesystems                                                 success
	    [✓] Updating icon theme cache: hicolor                                  success
	    [✓] Updating desktop database                                           success
	    [✓] Updating manpages database                                          success

    Press enter to continue

### Removing a package

  Removing a package uninstalls a package. This is what it looks like if I install Minetest:

      The following list of packages will be removed
      in the respective order to satisfy dependencies:
	  minetest
	  Removing package minetest
	  Removed minetest
	     [✓] Syncing filesystems                                                success
	     [✓] Updating icon theme cache: hicolor                                 success
	     [✓] Updating desktop database                                          success
	     [✓] Updating manpages database                                    	    success

	  Press enter to continue

### Updating all packages

Updating all packages updates EVERYTHING ON THE SYSTEM. Here's what it looks like when you have nothing to upgrade:

	  Updating repositories
	  Updating repository: Solus

	  eopkg-index.xml.xz.sha1sum     (40.0  B)100%    289.47 KB/s [00:00:00] [complete]
	  Solus repository information is up-to-date.
	  No packages to upgrade.

	  Press enter to continue

### Updating the repository

Updating the repository, checks the repository for new versions of packages. It is recommended to do this before updating. Here it looks like when the repository is up-to-date:

	  Updating repository: Solus
	  eopkg-index.xml.xz.sha1sum     (40.0  B)100%    394.80 KB/s [00:00:00] [complete]

	  Solus repository information is up-to-date.

	  Press enter to continue

### Cleaning

Cleaning helps save hard drive space. It does this by deleting cache, and deleting unneeded dependencies. Here is what it looks like:

	  Cleaning package cache /var/cache/eopkg/packages...
	  Cleaning source archive cache /var/cache/eopkg/archives...
	  Cleaning temporary directory /var/eopkg...
	  Removing cache file /var/cache/eopkg/installdb.cache...
	  Removing cache file /var/cache/eopkg/componentdb.cache...
	  The following list of packages will be removed
	  in the respective order to satisfy dependencies:
	  irrlicht
	  Do you want to continue? (yes/no)yes
	  Removing package irrlicht
	  Removed irrlicht
	     [✓] Syncing filesystems    			                                      success
	     [✓] Updating dynamic library cache                                     success

	  Press enter to continue

## Changing the package manager

### Temporarily (On Linux, BSD, and macOS.)

To Temporarily change the package manager used, use an argument. For example, if I wanted to temporally change it to apt-get, I would type

    sudo termget apt-get

### Permanently (On Linux, BSD, and macOS)
run the following command in a terminal, then the first setup script will start next time you run termget.

    rm -rf ~/.termget/termget-package-manager && > ~/.termget/termget-package-manager


## Installing TermGet on Windows
TermGet isn't out for Windows yet.

## License

Licensed under LGPLv3

The license is stated in the LICENSE document on the root directory
