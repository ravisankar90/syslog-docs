##Typical syslog.conf for all linux variants
This document contains the list of typical & most essential logs to be generated with syslog. You can use this to edit your syslog.conf file. Just copy the content in type column, put it in the file & put the content in Log File column in corresponding row with a space or a tab. 

|Type|Log File|Remarks| 
|---|---|---|
|kern.err|/var/log/nxsensor/kernel.err|Every logs of severity 3 to 0. Logs error, critical, alert & emergency messages related to kernel.|
|daemon.=info;daemon.=notice;daemon.=warning|/var/log/nxsensor/daemon/daemon.info|Logs info, notice & warning messages related to system daemons like bro, httpd, crond etc|
|daemon.err|/var/log/nxsensor/daemon/daemon.err|Logs all messages equal to  & higher than error priority from daemons|
|user.*|/var/log/nxsensor/user.log|All logs from user to the destination file|
|kern.crit|@remotehost|/var/log/nxsensor/kern.crit|Sends all logs >= level 2 to a remote host in case of kernel failure. In such cases, device may not respond or disk cannot be read. |
|auth.crit|/var/log/nxsensor/auth/auth.crit|Logs all messages >= level 2 to destination file|
|auth.=debug;=info;=notice;=warn;=err|/var/log/nxsensor/auth/auth.message|Logs all messages other than Critical alert & emergency from auth to destination file.|
|authpriv.err|/var/log/nxsensor/authpriv|Logs all messages of priority >=3 from auth priv.|
|ntp.warning|/var/log/nxsensor/ntp|Logs NTP messages >= 4|
|cron.=debug;=info;=notice;=warn|/var/log/nxsensor/cron/cron.warn|Logs CRON messages of priority < 3|
|Cron.err |/var/log/nxsensor/cron/cron.crit|Logs CRON messages of priority >= 3|
|mail.*|/var/log/nxsensor/mail.log|Logs all messages related to mail.|

