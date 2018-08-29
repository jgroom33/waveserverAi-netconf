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
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=license/activate-license-file.xml
# get Reg id
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=license/set-reg-id.xml
```

### Software upgrade

rpc located: [software](software)

```bash
# Install (Download, Activate, Commit) software from URL
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=software/install.xml
# Get Software information
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=software/get-software.xml
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
# Set Hostname
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=configuration/Sethostname.xml
```

### PTP

rpc located: [ptp](ptp)

```bash
# Set PTP properties 
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=port/setptpproperties.xml
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
### Warm and Cold Restart Chassis

Commands print their output to restart.xml

rpc located: [chassis](chassis)

```bash
# Restart Waveserver Ai
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=chassis/restart.xml > restart.xml
# Cold Restart Waveserver Ai
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=chassis/restart-cold.xml > restart.xml
```
### Warm and Cold Restart Modules

Commands print their output to restart.xml

rpc located: [module](module)

```bash
# Cold Restart Waveserver Ai
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=module/module-cold-restart.xml > restart.xml
# Warm Restart Waveserver Ai
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=module/module-warm-restart.xml > restart.xml
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

rpc located: [system/lamp-test](system/lamp-test)

```bash
# Disable Lamp Test Chassis
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=chassis/lamp-test/lamptest-chassis-disable.xml
# Enable Access Panel Chassis
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=chassis/lamp-test/lamptest-chassi-enable.xml
# Disable Lamp Test slot
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=chassis/lamp-test/lamptest-slot-disable.xml
# Enable Access Panel slot
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=chassis/lamp-test/lamptest-slot-enable.xml
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
# Set SysLog
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=aaa/syslog.xml
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
### SNMP
rpc located: [snmp](snmp)

```bash
# Set SNMP Target
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=snmp/snmptarget.xml
# Set SNMP community
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=snmp/setcommunity.xml
# Set SNMP Target-params
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=snmp/setsnmptarget-params.xml
# Set SNMP Create
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=snmp/snmpcreate.xml
# Set SNMP get
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=snmp/snmpget.xml
```
### XCVR
rpc located: [xcvr](xcvr)

```bash
# Get Actual Mode
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=xcvr/getactualmode.xml
# Get Operational Mode
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=xcvr/getoperationalmode.xml
# Set Waveserver XCVR properties 
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=xcvr/setwsxcvrproperties.xml
# Set xcvr mode 56-200
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=xcvr/setxcvrmode56-200.xml
# Set xcvr mode 56-400
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=xcvr/setxcvrmode56-400.xml
# Set xcvr mode 56-300
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=xcvr/setxvcrmode56-300.xml
```

### port
rpc located: [port](port)

```bash
# Set Ethernet properties
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=port/setethernetproperties.xml
# Set OTN properties
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=port/setotnproperties.xml
# Set Port properties 
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=port/setportproperties.xml
# Set Channel properties 
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=port/setchannelproperties.xml
# Set Laseroff Conditioning
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=port/laseroffconditioning.xml
# Set Ethernet Port Conditioning
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=port/ethernetportconditioning.xml
# Set None Port Conditioning
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=port/none-portconditioning.xml
# Set OTN Port Conditioning
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=port/otnportconditioning.xml
```