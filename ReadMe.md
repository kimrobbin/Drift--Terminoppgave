Setup for a Small to Medium-Sized Company

# 1. Plan

The plan is to set up infrastructure for a small to medium-sized company.
The infrastructure will be a combination of both physical and virtual machines.

# 2. Needed Hardware

The needed hardware is as follows:

* 1 Firewall
* 2 Servers
* 1 Test PC

# 3. Needed Software

The needed software is as follows:

* OPNsense
* Windows Server 2022
* Hyper-V

# 4. The Setup

### First Server

1. Install Windows Server 2022
 * Name the computer (e.g., "Server1")
 * Set a static IP address
 * Activate Hyper-V
 * Activate Active Directory Domain Services (ADDS)
    * Activate Domain Name System (DNS)
    * Activate Dynamic Host Configuration Protocol (DHCP)

### After Rebooting the Server

1. Install the Firewall
 * Open Hyper-V Manager and create a new virtual switch with a VLAN
 * Install OPNsense on a virtual machine
 * Configure OPNsense to use 2 virtual switches. One of them needs a VLAN
 * Start the OPNsense virtual machine without secure boot
 * Finish the installation of OPNsense
    * Make sure that the `Wan` does not have the `VLAN` tag and the `LAN`  hase the `VLAN` tag
	* Remember to make OPNsense boot from disk 
  
2. Configuration of the Active Directory Domain Services
 * Go to mange and click roles and features

### Second Server

1. Install Windows Server 2022
 * Name the computer (e.g., "Server2")
 * Set a static IP address
 * Activate Hyper-V
 * Join the server to the Active Directory domain
 * Configure disk redundancy (e.g., RAID 1)

### Test PC

1. Install a client operating system (e.g., Windows 10/11)
 * Join the Domain
 * Do a internet speed test
 * Check the share folder
