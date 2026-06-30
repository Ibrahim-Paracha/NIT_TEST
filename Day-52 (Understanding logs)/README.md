# Module 6 / 28-June-2026, Sunday

`systemctl` if you want to check the status of an agent/daemon eg `systemctl status sshd`
ssh is a service to get into the system, while sshd is the agent inside the system, ssh isn't found within the system, since its just used to get into the system.
`systemctl enable/disable agent` if sshd agent is disabled, and you reboot it, then you cant ssh into the machine anymore.
So a Linux admin always checks the status of the agent before patching and rebooting a system.
SLA = Service Level Agreement (Levels of tickets that are raised from high priority to lower priority)(not very important at this point)
enabling a service is at boot time, once enabled, it can be started, stopped, restarted or rebooted, when changes are done in the config files, then you can start.

## /var folder 
where all the logs are stored, all events like timestamps, errors etc, if this gets full, you can either get more storage, or the more logical way to prevent it from filling up would be to decide a good amount of storage to stay at and 

rsyslog listens for log messages from the kernel, services and apps, like who logged in etc, and dumps it in into the /var/log/messages folder. this is good for just one machine, while journalctl is much faster, its a centralized binary database, it has indexing, unlike rsyslog, so it can instantly find a log. eg `journalctl -u cloudflared -n 50 --no-pager` (cloudflare is a service, d is the daemon, n is for number of lines, no pagers means to just print the output on the screen rather than opening it in a scrollable viewer)

`tail -f /var/log/messages` - to see the logs in real time, this can be tested by typing this command in one tab, while entering the logger command in a another

logger command to inject a log on purpose. eg `logger "Hello world!"`

SEIM - Security Information and Event Management

logrotate - log management tool, renames logs, compresses old logs, deletes old logs and prevents var/logs from filling up
`logrotate.conf logrotate.dtouch`