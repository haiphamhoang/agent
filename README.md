# HetrixTools Linux Server Monitoring Agent

```
wget https://raw.githubusercontent.com/haiphamhoang/hetrixtools-agent-install/2.0.x-eth0/hetrixtools_install.sh && bash hetrixtools_install.sh YOURID 0 0 0 0 0 0

wget https://raw.githubusercontent.com/haiphamhoang/hetrixtools-agent-install/2.0.x-eth0/hetrixtools_update.sh && bash hetrixtools_update.sh 

```

Fix when ipv6 error
```
wget --inet4-only --retry-connrefused --waitretry=1 -t 3 -T 15 -qO- --post-file="$ScriptPath/hetrixtools_agent.log" https://sm.hetrixtools.net/ &> /dev/null
```


Documentation available here: https://docs.hetrixtools.com/category/server-monitor/


-= ChangeLog =-

Version 2.0.9: 
- Fixed a bug where in some cases RAID would not be detected properly.

Version 2.0.8: 
- Added support for Custom Variables: https://docs.hetrixtools.com/server-agent-custom-variables/ 
- Fixed `needs-restarting` for CloudLinux 8 https://github.com/hetrixtools/agent/commit/7e87b191bab90f682d2f55cc0f2650b5f4f7e0c7 (thanks to @JLHC)

Version 2.0.7:  
- Improved CPU temperature reading by adding support for two third-party software `lm-sensors` and `ipmitool`.

Version 2.0.6:
- Improved the `servicestatus` function.

Version 2.0.5:
- Improved the `servicestatus` function.

Version 2.0.4:
- fixed a bug where data was not properly being formatted in some cases when monitoring running processes

Version 2.0.3:
- initial v2 release

Pre v2 changelog:  
https://github.com/hetrixtools/agent/tree/1.6.x
