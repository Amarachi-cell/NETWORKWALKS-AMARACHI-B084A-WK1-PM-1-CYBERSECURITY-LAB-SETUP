# NETWORKWALKS-AMARACHI-B084A-WK1-PM-1-CYBERSECURITY-LAB-SETUP
# Kali Linux VirtualBox Setup (NAT Network)

Quick setup guide on how I configured my Kali Linux virtual machine in VirtualBox using a *NAT Network* with the IP address:- 10.0.0.24

 (A) Creating the Virtual Network in VirtualBox

1. Open VirtualBox and go to Tools> “Network”

2. Click **Create** to add a new ”NAT Network”

3. ⁠Set the details:
   Name:- NATNetwork 
   IPv4 Prefix:-10.0.0.0/24
Click on enable DHCP. Then APPLY.

(B) Set Up the Virtual Machine

1. Click “New” in VirtualBox and set:
   * Name:* Kali-Linux
   * Type:* Linux | * Version:* Debian (64-bit)
   * RAM:* 6124mb
   * Disk:* 80 GB
System
* Motherboard: boot device order(BIOS only) Hard disk and optical 
* ⁠Processor:- 4CPUs
* ⁠Acceleration:- Nested paging.

Go to **Settings** > **Network**:
   * **Attached to:** “NAT Network”
   * **Name:** Select “NATNetwork”
1. Mount your **Kali Linux ISO** under **Settings** > **Storage** and start the installation.

(C) Set IP Address to “10.0.0.24”

Once Kali Linux is installed and running:

1. Click the **Network Icon** (top right) > **Edit Connections**.

2. Select your connection and click the **Gear Icon** (Settings).

3. Go to **IPv4 Settings** and change **Method** to **Manual**.

4. Click **Add** and enter:
   * **Address:** 10.0.0.24
   * **Netmask:** 24
   * **Gateway:** 10.0.0.1
   * **DNS:** 10.0.0.1
Click “Save” and reconnect.

 (D) Testing Network Connection

Open the Kali terminal and test your connection:

Verify your IP
Input:- ip addr 

Test connection
input:-
ping -c 4 10.0.0.1
ping -c 4 google.com

Take a snapshot, save and add description.
