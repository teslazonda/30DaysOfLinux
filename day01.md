# Day 1: The Journey Begins

### LPIC-1 Objectives 102.4 & 102.5

### Managing Debian packages.

I learned about package managers in Debian, install and uninstall commands and `aptget` , `aptchache`.

#### Commands learned:

Show the contents of a package: `dpkg -c <package.deb>`

Show the package version and dependencies: `dpkg -I <package.deb>`

Show IF the package is installed: `dpkg -s <package.deb>`

Verify IF the package is properly installed: `dpkg -V <package.deb>`

Remove the package from system WITHOUT deleting dependencies: `dpkg -r <package.deb>`

Reconfigure an installed package:
`dpkg-reconfigure <package.deb>`

Install a package:
`sudo apt install <package name>`
`sudo apt-get install <package name>`

Check package dependencies
`apt-cache depends <package name>`


#### Repositories

Packages are stored in /etc/apt/sources.list in some Debian distros.


### Managing Red Hat packages

#### Commands learned:

##### `rpm` commands

Check IF a package is installed: `rpm -q <package.architecture.rpm>`

Install a package: `rpm -i <package.architecture.rpm>`

Uninstall a package: `rpm -e <package.architecture.rpm>`

Upgrade, or install a package if previously uninstalled : `rpm -U <package.architecture.rpm>`

Check package Info: `rpm -qi <package.architecture.rpm>`

Check package dependencies: `rpm -qR <package.architecture.rpm>`


##### `yum` commands

Check IF a package is installed: `yum list <package name>`

Install a package: `sudo yum install <package name`

Update a package: `yum update <package name>`

Uninstall a package: `sudo yum remove <package name`

Check package Info: `yum info <package name`

Check package dependencies: `yum provides <package name`

Clean YUM cache directory: `yum clean all`


##### `zypper` commands


Review package repositories: `zypper lr`

Update repo information: `sudo zypper refresh`

Check IF a package is installed: `sudo zypper search -i <package name>`

Install a package: `sudo zupper install <package name>`

Update a package: `sudo zypper update <package name>`

Uninstall a package: `sudo zypper remove <package name`

Check package dependencies: `sudo zypper what-provides /PATH/to/PACKAGE`

Check package Info: `sudo zypper info <package name>`

Check if installed packages have their dependencies met: `sudo zypper verify`
