Setup for a small company

# 1. Plan 

The plan is to setup infrastructure for a small to medium-sized company. 
<br>
The infrastructure is to be a combination of both physical and virtual machines.

# 2. Needed hardware 

The Needed hardware is as followed:

* ```1 Firewall ```
* ```2 Servers ```
* ```1 Test pc  ```

<br>

# 3. Needed software 

The needed software is as followed:

* OPNsense
<br><br>
* Windows Server 2022
<br><br>
* Hyper-v
<br><br>

# 4.  The setup

The first server
    
* Install windows server 2022 
    * Name the computer somthing smart
    * Set ``static ip address``
    * activate ``Hyper-v``
    * activate ``Active Directory Domain Services``

After a reboot of the server, the next step is to install the firewall.

* Open Hyper-V manager and create a new virtual switch with a ``vlan ``
    * Install ``OPNsense`` on a virtual machine 
    * Configure the ``OPNsense`` to use the virtual switch created earlier
    * Start the ``OPNsense`` virtual machine without secure boot 
    * Finish the installation of ``OPNsense`` 



