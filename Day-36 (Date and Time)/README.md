# Day 36

To display just the date `date +"%Y-%m-%d"`
To display just the time `date +"%H:%M:%S"`
To display both time and date `date +"%A %d %B %Y %H:%M:%S"`

To change just the date (only as root) `date +%Y%m%d -s "20260615"`
To change just the time `date +%T -s "14:30:00"`
To change both the date and time together `date -s "2026-06-20 09:15:00"`

## To sync network time automatically
timedatectl status`
`systemctl status chronyd` (To see which service/daemon is currently running on the system and to see which NTP server your system is connected to)
`cat /etc/chrony.conf` (To see the NTP server configuration)
`chronyc sources -v` (^ next to a server means it is the current active NTP source)
`timedatectl`

==============================================

`ls -l /var/log` this shows the importance of keeping the time accurate, because having the wrong time can cause incorrect logs, backup failures etc.
Having the server time inaccurate can also cause a user to not be able to access the companies website.

=============================================

Whenever troubleshooting, always check `date`, `timedatectl`, and `uptime`