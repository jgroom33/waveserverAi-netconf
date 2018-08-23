# WaveserverAi_curated_Netconf

A curated collection of Netconf executions to Waveserver Ai

## Dependencies

[netconf-console](https://pypi.org/project/netconf-console/)

```bash
pip install netconf-console
```

## Usage

```bash
NETCONF_HOST=10.181.67.111
NETCONF_USER=su
NETCONF_PW=su
```

### Hello

Quick test to make sure you are connecting

```bash
# Hello
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --hello
```

### System
rpc located: [system](system)

```bash
# NTP disable
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=system/ntp_disable.xml
# NTP enable
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=system/ntp_enable.xml
# NTP get
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=system/ntp_get.xml
```
### Date and Time  
rpc located: [system](system)
```bash
# Set Date and Time  
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=system/date-time_set.xml
# Get Date and Time  
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=system/date-time_get.xml
```

### Licenses
rpc located: [license](license)
```bash
# get license
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=license/get-license.xml
# Activate license *note license file needed to be update on xml
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=/license/activate-license-file.xml
```

### Software upgrade

rpc located: [software](software)

```bash
# Install (Download, Activate, Commit) software from URL
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=software/install.xml
```

### Configuration
rpc located: [configuration](configuration)
```bash
# Configuration  save
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=configuration/config-save.xml
# Configuration install
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=configuration/config-install.xml
# Configuration reset to user config
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=configuration/config-reset-to-user-config.xml
# Configuration delete
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=configuration/config-delete.xml
```
### Encryption
Commands print their output to getsharedkey.xml

rpc located: [encryption](encryption)

```bash
# Setup Pre-Shared Key
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=encryption/pre-sharedkey.xml
# Get Pre-Shared Key
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=encryption/get-presharedkey.xml > getsharedkey.xml
```
### Warm and Cold Restart

Commands print their output to restart.xml

rpc located: [chassis](chassis)

```bash
# Restart Waveserver Ai
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=chassis/restart.xml > restart.xml
# Cold Restart Waveserver Ai
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=chassis/restart-cold.xml > restart.xml
```

### Alarms

Commands print their output to alarms.xml

rpc located: [alarm](alarm)

```bash
# Get Alarms
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=alarm/get-alarms.xml > alarms.xml
```

### PMs

Commands print their output to output.xml

rpc located: [pm](pm)

```bash
# Get Ethernet
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-pm-ethernet.xml > ethernet-pm.xml
# Get Modem PMs
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-pm-modem.xml > modem-pm.xml
# Get ODU PMs
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-pm-odu.xml > odu-pm.xml
# Get OTU PMs
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-pm-otu.xml > otu-pm.xml
# Get optical PMs
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-pm-optical-power.xml > optical-pm.xml
# Get PM Config
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-global-config.xml > pm-config.xml
```

### Lamp Test

rpc located: [chassis/lamp-test](chassis/lamp-test)

```bash
# Disable Access Panel
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=chassis/lamp-test/panel-disable.xml
# Enable Access Panel
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=chassis/lamp-test/panel-enable.xml
```


### User Get/Create/Delete
rpc located: [aaa](aaa)

```bash
# User get
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=aaa/user_get.xml
# user create
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=aaa/user_create.xml
# user delete
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=aaa/user_delete.xml
```
### Loopback
rpc located: [loopback](loopback)

```bash
# Disable Port
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=loopback/port-disable.xml
# Disable Loopback
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=loopback/disable-loopback.xml
# Rx Loopback
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=loopback/rx-loopback.xml
# Tx Loopback
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=loopback/tx-loopback.xml
# Get Loopback
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=loopback/get-loopback.xml > loopback.xml
# Enable Port
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=loopback/port-enable.xml
```