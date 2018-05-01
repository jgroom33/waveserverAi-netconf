# WaveserverAi_curated_Netconf

A curated collection of Netconf executions to Waveserver Ai

## Dependencies

[netconf-console](https://pypi.org/project/netconf-console/)

```bash
pip install netconf-console
```

## Usage

```bash
NETCONF_HOST=10.132.241.92
NETCONF_USER=su
NETCONF_PW=su
```

### Hello

Quick test to make sure you are connecting

```bash
# Hello
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --hello
```

### Alarms

Commands print their output to output.xml

rpc located: [get-alarms.xml](alarm/get-alarms.xml)

```bash
# Get Alarms
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=alarm/get-alarms.xml > output.xml
```

### PMs

Commands print their output to output.xml

rpc located: [pm](pm)

```bash
# Get Ethernet
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-pm-ethernet.xml > output.xml
# Get Modem PMs
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-pm-modem.xml > output.xml
# Get ODU PMs
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-pm-odu.xml > output.xml
# Get OTU PMs
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-pm-otu.xml > output.xml
# Get optical PMs
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-pm-optical-power.xml > output.xml
# Get PM Config
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-global-config.xml > output.xml
```

### Chassis

rpc located: [chassis/lamp-test](chassis/lamp-test)

```bash
# Disable Access Panel
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=chassis/lamp-test/panel-disable.xml
# Enable Access Panel
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=chassis/lamp-test/panel-enable.xml
```

rpc located: [chassis](chassis)

```bash
# Restart Waveserver Ai
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=chassis/restart.xml > output.xml
# Cold Restart Waveserver Ai
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=chassis/restart-cold.xml > output.xml
```

### Software upgrade

rpc located: [software](software)

```bash
# Install (Download, Activate, Commit) software from URL
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=software/install.xml
```

### System

```bash
# NTP disable
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=system/ntp_disable.xml
# NTP enable
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=system/ntp_enable.xml
# NTP get
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=system/ntp_get.xml
```

```bash
# NTP disable
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=system/date-time_set.xml
# NTP enable
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=system/date-time_get.xml
```

### AAA

```bash
# User get
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=aaa/user_get.xml
# user create
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=aaa/user_create.xml
```
