# Day 4: Customizing Your Shell Environment

## LPIC-1 Objective 105.1
<br></br>

### Notes

Global environment files:

* `/etc/profile`
* `/etc/profile.d`
* `/etc/bashrc`
* `/etc/bashrc.bashrc`

Local environment files:

* `~/.bash_profile`
* `~/.bash_login`
* `~/.profile`
* `~/.bashrc`
* `~/.bash_logout`

These local environment files are hidden files. They can be viewed with `ls -a`.

#### Local environment file selection

* The first file in list is run, and the rest are ignored:

    1. `~/.bash_profile`
    2. `~/.bash_login`
    3. `~/.profile`

* This file typically run by other environment files: `~/.bashrc`



