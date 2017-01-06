# Template_F5_SNMP

## Data
The template uses SNMP to get the following data from the F5

1. CPU
2. Memory
3. Network performance
4. SSL performance (TPS, protocols, errors)
5. Virtual Servers, Pools (Discovered automatically)
 
## Triggers 
The following triggers are defined

1. High CPU utilization
2. Out of sync configuration state
3. Low free TMM memory 
4. Node/Pool/Virtual Server is disabled
5. Node/Pool/Virtual Server is down or unavailable

## Usage
Using the template

1. Download SNMP MIBs from a F5 device, place in your Zabbix server and Zabbix proxy SNMP MIB directory and restart the service
2. Configure {$SNMP_COMMUNITY} Macro under the host in Zabbix
3. Create matching SNMP Community on your F5 device and add the Zabbix server and proxy IP to the allowed hosts
4. Import template

## Notes
1. If you are using Zabbix 2.x configure the Value maps manually before importing the template
2. Tested with F5 version 11.x SNMP MIBs and F5 version 11.x/12.x devices
