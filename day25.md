# Day 25: Linux Network Manager cont

## LPIC-1 Objective 109.2 and 109.3
<br></br>

## Notes

Change to a static ipv4 address: `sudo nmcli connection modify id '<name of connection>' ipv4.method manual -a`

Restart the connection: `sudo nmcli connection up id '<name of connection>'`

Check that the static IP address has changed: `ip -br addr show`

Change the hostname: `sudo nmcli general hostname <newhostname>`
