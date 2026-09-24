# Lab-2.a
Male an ubuntu vm and write a systemd service that tuns as a dedicated non-root user on a timer


2. i did not somehow run in to an error? atleast one desribed in the lesson work. i did get confused about the service account
that my putput didnt match expected output but using "sudo usermod -g 999 reports" it fixed it

3. Well i didn thvae the problem but i would use chown since it looks easier to use and automates the problem for me,
maybe thast why i dint run in to error since i used it before verying if ran correcly.

rasmus@rasmus:~$ systemctl show disk-report.service -p User
User=reports
rasmus@rasmus:~$ systemctl is-enabled disk-report.service
systemctl is-enabled disk-report.timer
static
enabled
rasmus@rasmus:~$ systemctl list-timers disk-report.timer
NEXT                        LEFT LAST                           PASSED UNIT              ACTIVATES
Fri 2026-09-25 00:00:00 UTC  17h Thu 2026-09-24 06:20:13 UTC 14min ago disk-report.timer disk-report.service

1 timers listed.
Pass --all to see loaded but inactive timers, too.
rasmus@rasmus:~$ systemctl list-timers disk-report.timer
NEXT                        LEFT LAST                           PASSED UNIT              ACTIVATES
Fri 2026-09-25 00:00:00 UTC  17h Thu 2026-09-24 06:20:13 UTC 14min ago disk-report.timer disk-report.service

1 timers listed.
Pass --all to see loaded but inactive timers, too.
rasmus@rasmus:~$
