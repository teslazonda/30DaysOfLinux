# Day 8: Managing Users and Groups cont.

## LPIC-1 Objective 107.2
<br></br>

### Notes

A user's primary group id is set upon logging into the system.

List all the current groups the current user is a member of: `groups`

Command shows user's current primary group: `id -gn`

Command changes user's current primary group: `newgrp <groupname>`

Use this command to get the id of the user's primary group, which is stored in the password file: `getent passwd <user>`

Use the id of a group to get the name of a group: `getent group <group id>`

Use the following command to add a user to a group without setting a group password: `sudo usermod -aG <group> <user>`

#### The group Database

Data on groups is stored in `/etc/group`. The records look like: `wheel:x:7:joe`. These fields are as follows:

1. Group name (unique)
2. Password (now stored in `/etc/gshadow`)
3. Group ID number
4. Group members (if any)

### Adding Groups

`sudo groupadd <groupname>`

It is good practice NOT to set group passwords.

Change a group name: `sudo groupmod -n <newname> <current-groupname>`

Delete a group with: `sudo groupdel <groupname>`
