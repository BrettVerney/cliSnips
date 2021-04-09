CLI Snippet by Brett Verney (@wifiwizardofoz)<br>
Version: v0.1 | 9-04-2021<br>
Used for: Common Regex patterns for searching and filtering Cisco IOS CLI output<br><br>

```show run | i ^interface|^_ip address```<br>
Shows all interfaces and their IP address information in an IOS style CLI formatReturns lines that being with 'interface' or  'ip address', essentially giving you all of your interface IP’s in an IOS-pastable format.<br><br>

```show ip int brief | e unassigned```<br>
Shows all layer 3 capable interfaces on the device.<br><br>
	
```show ip int brief | exclude ^G```<br>
	Show all interfaces that don't start with G (GigabitEthernet for example)<br><br>
	
```show ip int brief | include ^(G|I)```<br>
	Shows all interfaces that start with a G or I (Show the Interface heading, and only include Gigabit Interfaces)<br><br>

```show int status | i Gi[1-8]/0/24```<br>
	Shows the status of all port 24s on switches 1 through 8 in a multi chassis or stack setup<br><br>

```show int status | i Gi[127]/24```<br>
	Shows the status of all port 24s in slots 1, 2, and 7 in a multi chassis or stack setup<br><br>

```show int status | i Gi3/0/(15|2[0-4])```<br>
	Shows the status of ports 15 trhough 24 in switch 3 .<br><br>

```show interf status | i _15_```<br>
	Shows all of the interfaces assigned to VLAN 15<br><br>
	
```show int | include ^[A-Z]|Last in```<br>
	Best way to show the last time a frame entered an interface<br><br>

```show int status | i (a-half___a-10|a-half_____10|half_____10|a-full___a-10|full_____10|auto_____10|half_____100|a-half_____100)```<br>
	Shows all interfaces currently operating at 10Mbps and/or Half-Duplex<br><br>

```sh int status | inc (.*not.*154.*)```<br>
	Shows interfaces not connected and assigned to VLAN 154<br><br>
	
```sh int count err | e 0___________0___________0___________0__________0____________0|0__________0__________0___________0__________0__________0__________0```<br>
	Show all interfaces that have had errors since the last reboot or interface counter reset<br>

```show cdp ne de | i -|e ID|Interface:|IP add|Plat```<br><br>
	Summarise the cdp neighbor detail output<br>
	
```show lldp ne de | i is id|al In|em na|IP:|em De|rt De```<br>
	Summarise the lldp neighbor detail output<br><br>


