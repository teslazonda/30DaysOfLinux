# Day 10: Scheduling Jobs with a cron table

## LPIC-1 Objective 107.2
<br></br>

### Notes

### User crontab record format

Sample: `30 1 31 31 21 * /home/somescript.sh`

Crontab records have six fields:

1. Minute passed the hour (0-59)
2. Hour of the day (0-23)
3. Day of the month (1-31)
4. Month of the year (1-12) || Can also use three letter names of months (jan,feb,mar)
5. Day of the week (0-7, Sunday is 0 or 7) || Can also use three letter names of the week (sun,mon,tue)
6. Command to run

Asterisks represent all

Run a job at 15 minutes past the hour every hour: `15 * * * * <command>`

#### Editing the User cron Table

`crontab -e`
The following is an example entry, running the `df` command at 14:15 everyday.

```
SHELL=/bin/bash
MAILTO=<username>
15 14 * * * /bin/df
```

`crontab -l` view current user cron table.

`crontab -r` delete current user cron table.

### System crontab records

1. Minute passed the hour (0-59)
2. Hour of the day (0-23)
3. Day of the month (1-31)
4. Month of the year (1-12) || Can also use three letter names of months (jan,feb,mar)
5. Day of the week (0-7, Sunday is 0 or 7) || Can also use three letter names of the week (sun,mon,tue)
6. Account to run command
7. Command to run

Stored in `/etc/cron.d`

There are also different directories for each time span, (hourly, daily, etc) `/etc/cron.*`
