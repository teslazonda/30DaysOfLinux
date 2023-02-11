# Day 12: Scheduling Jobs with systemd

## LPIC-1 Objective 107.2
<br></br>

### Notes

Systemd timers can be monotonic or in real time. This means they can be set relative to an event, such as the system booting up, or be set to run at a specific time.

Run job 20 seconds after the system boots: `OnBootSec=20s`

Run a job every Wednesday at 2:30pm: `OnCalendar=Wed*-*-* 14:30:00`
