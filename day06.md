# Day 6: Managing Users and Groups

## LPIC-1 Objective 107.1
<br></br>

### Notes

DAC - Discretionary Access Control. Access to items based on username and group membership.


#### Passwords

Using the `sudo getent shadow <user>` we can check if a password is set for a user account. 

There are four fields in the record returned by this command.

1. Username (Same as in password record).
2. Password (hashed).
    * If no password is set `!!` or `!`.
    * Cannot log into account `!` or `*`.
    * `!` before password hash means the account is locked.
3. Last date password was changed (Epoch date format).
4. Minimum days between password changes.
5. Days until password expires.
6. Days of warning before password expires.
7. Days until account is deactivated after password expires.
8. Account expiration date.
9. Special Flag (Not currently used; reserved for future use).  

<br></br>

#### Changing Passwords

`sudo passwd <username>`

Passwords on modern systems are almost always displayed as a hash.

To view information about when a password was set and password expiry in a human readable form: `sudo passwd -S <username>`

To lock an account: `sudo passwd -l <username>`.
To unlock an account: `sudo passwd -u <username>`.






