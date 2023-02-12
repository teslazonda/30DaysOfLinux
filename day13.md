# Day 13: Understanding Time Management

## LPIC-1 Objective 108.1
<br></br>

## Notes

### Setting the Time

Coordinated Universal time (UTC)

Linux uses UTC time, but displays time as Local time.

There are two types of clocks:
1. Hardware clock - not super accurate, so network syncing is often used.
2. Software clock

Clock commands:`hwclock`, `date`, `timedatectl`

`sudo hwclock --show`
The hardware clock: `sudo hwclock -r`
The software clock: `date`

We can adjust the hardware clock for systems that have spent large amounts of time offline with the following command: `sudo hwclock --adjust`

For systemd systems: `timedatectl` displays UTC, Local time, hardware clock and sync.

Set the software clock with :

1. `sudo timedatectl set-time "CCYY-MM-DD HH:mm`
2. `sudo date --utc date/time`
3. `sudo hwclock --systohc`


### Setting the Time Zone

Displays current time in Local Time: `date`

Shows time zone, daylight savings (if enacted)`timedatectl`

Time Zone information is located in `/etc/share/zonein`

`/etc/timezone` File on Ubuntu that shows time zone information.

We can change the time zone by changing the soft link on `/etc/localtime` with this command: `ln -sf usr/share/zoneinfo/Continent/Zonename /etc/localtime`

#### The `tzselect` utility

Shows you how to set the `$TZ` environment variable locally for your desired timezone.


### NTP and the NTP daemon

NTP stands for Network Time Protocol.

NTP hierarchy:

* Atomic clocks are stratum 0, the most accurate time keeping devices. The only NTP servers allowed to receive time information from stratum 0, are stratum 1 NTP servers

* Stratum 2 servers receive time data from stratum 1 servers.

* Stratum 3 servers receive time date from stratum 2 servers etc.

The NTP pool: The solution to abuse of stratum 1 NTP servers.

1. Stratum 3 and 4 data is pooled into distribution zones, large groups of NTP servers.

2. We can select which group of NTP pools to pull time data from based on our location and distribution.

`chrony` is the new version of the `NTP` daemon.

Check the status of the NTPD daemon: `systemctl status ntpd`

We can implement accurate time with NTP in six steps:

1. Select a pool zone - The closer the more accurate.

2. If needed, modify the NTP configuration file: `/etc/ntp/conf`
  * `grep ^server /etc/ntp.conf` - shows the NTP server pools selected. Up to 4 on centos.

3. If needed, eliminate insane time (when your system clock is more than 17 minutes different from acutual time).
  * If your system has insane time, the NTP daemon will NOT update your system time.

  * To fix use: `ntpdate <ntp-pool-url>`

4. Start (or restart) the NTP daemon.
  * Make sure the system will run the NTP daemon on boot with: `sudo systemctl enable ntp`

5. Check the time synchronization status with: `ntpstat`

6. Optional - periodically check the NTP pool zone choices: `ntpq -p`

### `chrony` daemon

`sudo apt-get install chrony`

1. Select a pool zone

2. Modify chrony configuration file: `/etc/chrony.conf` or `/etc/chrony/chrony.conf` the servers are called _pool_ in the .conf file.

3. Start the chrony daemon (and enable, if needed). `systemctl status chrony`. `systemctl start chrony`.

4. Check on with `chronyc tracking`

5. Check on with `chronyc sources -v`



