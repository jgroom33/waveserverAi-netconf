# WaveserverAi_curated_Netconf

A curated collection of Netconf executions to Waveserver Ai

## Dependencies

[netconf-console](https://pypi.org/project/netconf-console/)

```bash
pip install netconf-console
```


## Usage

```bash
NETCONF_HOST=10.181.36.238
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
# get license List
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=license/get-license-list.xml
# get license instances
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=license/license-alarm-instances.xml
# get Reg id
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=license/get-reg-id.xml
# Activate license *note license file needed to be update on xml
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=license/activate-license-file.xml
# set Reg id
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
# Configuration reset to factory
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=configuration/reset-to-factory-default.xml
# Configuration delete
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=configuration/config-delete.xml
# Set Hostname
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=configuration/Sethostname.xml
# Set System shell (inactivity time, banner)
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=configuration/Set-system-shell.xml

```

### PTP

rpc located: [ptp](ptp)

```bash
# Set PTP properties 
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=ptp/getPTP.xml
# Get frequency
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=ptp/getfrequency.xml
# Get PTP power 
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=ptp/getPower.xml
# Set PTP frequency
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=ptp/setfrequency.xml
# Set PTP disable,frequency & Power to 191342.5
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=ptp/freq-power-set.xml
# Set PTP disable,frequency & Power to 0
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=ptp/disable-ptp-freq0.xml
# Enable PTP  
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=ptp/enable-ptp.xml
# Disable PTP  
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=ptp/disable-ptp.xml
# Set PTP power (Run after Frequency State is up)
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=ptp/setPower.xml
# Set Frequency & Power
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=ptp/freq-power-set.xml
```
### Encryption
Commands print their output to getsharedkey.xml
rpc located: [encryption](encryption)

```bash
# Setup Pre-Shared Key
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=encryption/pre-sharedkey.xml
# Get Pre-Shared Key
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=encryption/get-channel-encryption.xml > output/getsharedkey.xml
```

### User Get/Create/Delete/Syslog
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

### Lamp Test

rpc located: [system/lamp-test](system/lamp-test)

```bash
# Disable Lamp Test Chassis
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=system/lamp-test/lamptest-chassis-disable.xml
# Enable Lamp Test Chassis
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=system/lamp-test/lamptest-chassi-enable.xml
# Disable Lamp Test slot
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=system/lamp-test/lamptest-slot-disable.xml
# Enable Lamp Test slot
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=system/lamp-test/lamptest-slot-enable.xml
```
### PMs

Commands print their output to output.xml

rpc located: [pm](pm)

```bash
# Set PM State
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/pm-admin-state-disable.xml
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/pm-admin-state-enable.xml
# Set PTP State
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/ptp-pm-state-disable.xml
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/ptp-pm-state-enable.xml
# Set Modem-pm-enable
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/modem-pm-enable.xml
# Clear ptp PM
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/pm-clear-ptp.xml
# Clear Port PM
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/pm-clear-port.xml
# Clear Channel PM
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/pm-clear-channel.xml
# Get PM Config
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-global-config.xml
# Get PM Instance autocreated
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-pm-instance-autocreated.xml
# Get PM
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-pm.xml
# Get Ethernet
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-pm-ethernet.xml > output/ethernet-pm.xml
# Get Modem PMs
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-pm-modem.xml > output/modem-pm.xml
# Get ODU PMs
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-pm-odu.xml > output/odu-pm.xml
# Get OTU PMs
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-pm-otu.xml > output/otu-pm.xml
# Get optical PMs
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-pm-optical-power.xml > output/optical-pm.xml
# Get Encryption-gcm-pm-instance history
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-encryption-gcm-pm-instance-history.xml > output/pm-encrypt-config.xml
# Get Encryption-gcm-pm-instance Untimed bin
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-encryption-gcm-pm-instance-history-untimed-bin.xml > output/Encrypy-pm-untimed.xml
# Get Encryption-gcm-pm-instance Current bin
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-encryption-gcm-pm-instance-history-current-bin.xml > output/Encrypy-pm-current.xml
# Get Encryption-gcm-pm-instance 24 hour bin
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-encryption-gcm-pm-instance-history-24Hour-bin.xml > output/Encrypy-pm-24hr.xml
# Get Ethernet PM History
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-ethernet-pm-history.xml > output/eth-pm-his.xml
# Get Optical PM 24 hr History
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/get-optical-power-history-24-hours.xml > output/optical-pm-24.xml
# Get OTU
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=pm/otu-pm-history.xml > output/pm-otu.xml
```

### PORT
rpc located: [port](port)

```bash
# Get Ports
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=port/getPort.xml > output/getportoutput.xml
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
# Set Conditioning holdoff
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=port/conditioningholdoff.xml
```
### Alarms

Commands print their output to alarms.xml

rpc located: [alarm](alarm)

```bash
# Get Alarms
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=alarm/get-alarms.xml > output/alarms.xml
# Get Alarms Active
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=alarm/get-alarm-active.xml > output/alarms-act.xml
# Get Alarms History
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=alarm/get-alarm-history.xml > output/alarms-his.xml
# Get Alarms Statistics
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=alarm/get-alarm-statistics.xml > output/alarms-st.xml
```

### XCVR
rpc located: [xcvr](xcvr)

```bash
# Get Diagnostics
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=xcvr/getdiagnostics.xml > output/getdiagnosticsoutput.xml
# Get Actual Mode
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=xcvr/getactualmode.xml > output/getactualmodeoutput.xml
# Get Operational Mode
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=xcvr/getoperationalmode.xml > output/getoperationalmodeoutput.xml
# Set Waveserver XCVR properties 
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=xcvr/setwsxcvrproperties.xml
# Set xcvr mode 56-200
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=xcvr/setxcvrmode56-200.xml
# Set xcvr mode 56-400
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=xcvr/setxcvrmode56-400.xml
# Set xcvr mode 56-300
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=xcvr/setxvcrmode56-300.xml
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
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=loopback/get-loopback.xml > output/loopback.xml
# Enable Port
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=loopback/port-enable.xml > output/getportoutput.xml
```
### Maintenance
rpc located: [maintenance](maintenance)

```bash
# System State Dump
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=maintenance/system-state-dump.xml
# XFTP Setup
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=maintenance/system-xftp.xml
# Configuration backup
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=maintenance/configuration-backup.xml

```
### Warm and Cold Restart Chassis

Commands print their output to restart.xml

rpc located: [chassis](chassis)

```bash
# Restart Waveserver Ai
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=chassis/restart.xml > output/restart.xml
# Cold Restart Waveserver Ai
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=chassis/restart-cold.xml > output/restart.xml
```
### Warm and Cold Restart Modules

Commands print their output to restart.xml

rpc located: [module](module)

```bash
# Cold Restart Waveserver Ai
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=module/module-cold-restart.xml > output/restart.xml
# Warm Restart Waveserver Ai
netconf-console --host=$NETCONF_HOST --user=$NETCONF_USER --password=$NETCONF_PW --port=830 --rpc=module/module-warm-restart.xml > output/restart.xml
```

## apt installs

```
sudo apt-get install libncurses5-dev python3-lxml build-essential python3-dev
```

