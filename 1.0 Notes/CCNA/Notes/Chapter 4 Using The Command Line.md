#### Exam Topics Covered
[[Exam Objectives#2.0 Network Access (20%)| 2.0 Network Access]]
 [[Exam Objectives#2.8 Describe network device management access (Telnet, SSH, HTTP, HTTPS, console, TACACS+/RADIUS, and cloud managed)|2.8 Describe network device management access (Telnet, SSH, HTTP, HTTPS, console, TACACS+/RADIUS and Cloud Managed)]]


## Key Terms
- Command Line Interface (CLI)
- Configuration Mode
- Enable Mode
- IOS
- IOSX
- Rollover Cable
- running-config file
- Secure Shell (SSH)
- startup-config file
- Telnet
- user mode
---

# Notes
# Accessing the Cisco Catalyst Switch CLI
## Cisco Catalyst Switches
**3 Productions Models**
- Cisco Catalyst Switches - normal enterprise equipment
- Cisco Nexus Switches - designed for data center use (faster ports, more high speed ports on a switch)
- Cisco Meraki Switches - GUI based, easier onboarding of devices.
#### Interface Naming ID Examples

| Speeds Supported | Common Name | Example Interface ID   | Valid Abbreviations |
| ---------------- | ----------- | ---------------------- | ------------------- |
| 10 Mbps          | Ethernet    | Ethernet 0/0           | E0/0, Et0/0, Eth0/0 |
| 10/100Mbps       | 10/100      | Fast Ethernet 0/1      | F0/01, Fa 0/1       |
| 10/100/1000Mbps  | 10/100/1000 | Gigabit Ethernet 1/0/1 | G1/0/1, Gi 1/0/1    |
| 1G/2.5G/5G/10G   | Multigig    | Ten Giga bit 1/0/2     | t1/0/2, Te1/0/2     |

## Accessing the Cisco IOS XE CLI

### The Operating system in Cisco Catalyst Switches
- Originally was CatOS when purchased by Cisco eventually migrated to Cisco IOS (Internetwork Operating System)
- Newest iteration is IOS XE but commands tend to work in both versions 
### Accessing the IOS XE CLI
- 3 Popular methods 
	- Console Connections (Physical)
	- Telnet - IP Network Connection
	- Secure Shell (SSH) - IP Network Connection
### Cabling the Console Connection
- 3 main Components
	- Physical console port on switch
	- Physical serial Port on PC
	- Cable to interface between the 2 
- Older Cables used a RJ45-DB9 Convertor with a UTP rollover cable
- Rollover PIn out
	- Pin 1 -> 8
	- Pin 2 -> 7
	- Pin 3-> 6
	- etc
### Configuring a Terminal Emulator
- All data in emulator is treated as text
- Default console port options
	- 9600 bits/second
	- No HW flow control
	- 8-Bit ASCII
	- No Parity BIt
	- 1 Stop Bit
- 8N1 :
	- 8 Bit ASCII
	- No Parity
	- 1 Stop Bit
### Accessing the CLI with Telnet and SSH
- Switch is SSH/Telnet Server
- SSH more secure than telnet as telnet is clear text
- SSS Port 22 and Telnet Port 23
### User and Enabled (Privileged) modes
- All 3 CLI access methods put user in Exec Mode also called user mode
	- allows view but no changes
	- Exec Mode means that when a command is input, we get text back regarding the result. 
- Cisco IOS also has a more powerful exec mode called privileged also knows as enable mode, allows the use of more powerful privliedged commands

> [!info] User mode vs Enabled mode
> if prompt ends in > user mode if # enable mode
### Password Security for CLI Access from the Console
- By default Cisco switches do not have a console password. 
- to configure console 
```
line console 0
```
### Accessing the CLI from the Web UI
- once configured the switch can be accessed at the designated IP and can have some configuration options for those not familiar with CLI
## CLI Help Features

| What is Entered?    | What the terminal spits back                                                   |
| ------------------- | ------------------------------------------------------------------------------ |
| ?                   | will show all help for commands in current mode (User,Enable)                  |
| *Command* ?         | space between will list all first parameter options for given command          |
| *com*?              | will give you list of commands that start with com                             |
| *command parm*?     | lists all parameter beginning with what paremeter info has been entered so far |
| *command par* (TAB) | will try and autocomplete command if enough is given to isolate to one command |
| *command parm1* ?   | list all next parameters with a small blurb                                    |

## The Debug and Show command
- the *show* command most popular, essentially will show currently know facts about the switches status
- Can be used with other commands such as 
~~~
show mac address-table dynamic
~~~
- debug command also tells about witch operational status but is a "dynamic" will update with messages. 
## Configuring Cisco IOS Software
- commands are enacted in real time, when a command is changed the running configuration of the device is changed. 
## Configuring submodes and contexts
- *user mode -> enable mode -> configuration mode -> enable mode -> user mode*
- *interface* is a submode of configuration 
- example * interface FastEthernet 0/1* will allow the user to configure this interface

##### Common Switch Configuration Modes

| Prompt                 | Name of Mode | Context setting commands to reach thie mode |
| ---------------------- | ------------ | ------------------------------------------- |
| hostname(config)#      | Global       | *configure terminal*                        |
| hostname(config-line)# | Line         | *line console 0<br>line vty 0 15*           |
| hostname(config-if)#   | Interface    | *interface type number*                     |
| hostname(config-vlan)# | VLAN         | *vlan number*                               |
## Storing Switch configuration files
*Cisco Switch Memory Types*
- RAM - Working memory and running Configuration
- FLASH - Cisco IOS Software
- ROM - Bootstrap Program
- NVRAM - Startup Configuration


| Configuration Filename | Purpose                                                                                                                            | Where It Is Stored |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ------------------ |
| startup-config         | stored the initial configuration used anytime the switch reloads Cisco IOS                                                         | NVRAM              |
| running-config         | stores the currently used configureation commands. The file changes dynamically when someone enters commands in configuration mode | RAM                |
- in configuration mode, changing the running-config file updates only the running config
- to keep config running-config needs to be copied over to the startup-config

## Copying and Erasing configuration Files
- 