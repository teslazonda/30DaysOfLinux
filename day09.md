# Day 9: Scheduling Jobs with the `at` Command

## LPIC-1 Objective 107.2
<br></br>

### Notes

The `at` command is used to run commands, or scripts at some future date.

The standard output of the mail command is to the `mail` system.

We can specify a time for the `at` utility to run a command with the following syntax: `HH:MM`, ex. 13:24.

Special times of day are: `noon`, `midnight`, and `teatime`(4PM).

If no date is specified, and the time hasn't passed yet, the command will run at that time today. If the time has passed already today, the command will run at that time tomorrow.

#### Date Formats

Movie date, hiking trip, rock concert... :)

* _Month day_ (June 9)
* _MMDDYY_ (080198)
* _MM/DD/YY_ (08/01/90)
* _YY-MM-DD_ (22-04-01)

Special dates: `now` `today` `tomorrow`

#### Offsets

We can offset the time a command runs with the following syntax: `<date/time> + <offset>`

The offset looks like this: `<count> <date/time-unit>`

The _date/time-unit_ can be

* minutes
* hours
* days
* weeks

For example `at today + 3 hours`


#### View Job Queue

`atq` shows commands waiting to be run by `at`.

#### Delete Jobs

Use the `atq` command to get the job number

Use `atrm <jobnumber>` to delete the job from the queue.


#### Access to `at` command

File name: `/etc/at.allow`. Usernames in this file are allowed to use `at`.

File name: `/etc/at.deny`. Usernames in this file are NOT allowed to use `at`.
