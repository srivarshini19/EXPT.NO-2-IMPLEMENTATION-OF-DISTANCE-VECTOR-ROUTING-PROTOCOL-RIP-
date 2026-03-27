# EXPT.NO-2-IMPLEMENTATION-OF-DISTANCE-VECTOR-ROUTING-PROTOCOL-RIP
# AIM:

To connect computers in multiple networks using Distance Vector Routing Protocol and to verify the connectivity between computers.

# EQUIPMENTS REQUIRED:

1.personal computer
2.cisco packet tracer 

# IP ASSIGNMENT:

<img width="475" height="219" alt="Screenshot 2026-03-19 at 1 35 56 PM" src="https://github.com/user-attachments/assets/1289d2b4-e280-4d9d-a960-72e30330a807" />


# NETWORK DIAGRAM:

<img width="914" height="362" alt="image" src="https://github.com/user-attachments/assets/0c1b5f16-937e-4384-ac97-67d00121a5bf" />

# PROCEDURE:

STEP 1: Open a Packet Tracer Software.

STEP 2: Drag two 2900 Switches, two Cisco 1800 Routers, four PC Terminals from tool barand drop it in work area.

STEP 3: Connect all the PC Terminals and Routers through Switches as shown in the networkdiagram using CAT 6 Patch cables.

STEP 4: Configure IP address and Gateway in all PC Terminals.

STEP 5: Configure ROUTER0 and restart ROUTER0.

STEP 6: Configure ROUTER1 and restart ROUTER1.

STEP 7: Verify the connectivity between PC Terminals in different networks using Pingcommand.

After This follow the given procedure

1. Assign IP Addresses to PCs
For each PC, go to Desktop > IP Configuration and assign:
o PC0: 192.168.1.2, Subnet Mask: 255.255.255.0, Gateway: 192.168.1.1
o PC1: 192.168.1.3, Subnet Mask: 255.255.255.0, Gateway: 192.168.1.1
o PC2: 192.168.2.2, Subnet Mask: 255.255.255.0, Gateway: 192.168.2.1
o PC3: 192.168.3.2, Subnet Mask: 255.255.255.0, Gateway: 192.168.3.1
o PC4: 192.168.4.2, Subnet Mask: 255.255.255.0, Gateway: 192.168.4.1
o PC5: 192.168.4.3, Subnet Mask: 255.255.255.0, Gateway: 192.168.4.1
 
# PROGRAM

   
RIP ROUTING CONFIGURATION

Router0

enable
configure terminal

interface FastEthernet0/0
ip address 192.168.1.1 255.255.255.0
no shutdown
exit

interface FastEthernet0/1
ip address 192.168.2.1 255.255.255.0
no shutdown
exit

router rip
version 2
network 192.168.1.0
network 192.168.2.0
exit

Router1

enable
configure terminal

interface FastEthernet0/0
ip address 192.168.3.1 255.255.255.0
no shutdown
exit

interface FastEthernet0/1
ip address 192.168.4.1 255.255.255.0
no shutdown
exit

router rip
version 2
network 192.168.3.0
network 192.168.4.0
exit


show ip route
   
   2.	Ping from PC to PC
   You can also check connectivity between the PCs on different networks to ensure that RIP is correctly routing packets across the routers.
   •	Example: Ping from PC0 (192.168.1.2) to PC3 (192.168.3.2):
   1.	Click on PC0, go to the Desktop tab.
   2.	Open the Command Prompt.
   3.	Use the ping command: ping 192.168.3.2
   4.	If everything is configured correctly, you should receive replies from PC3.
   •	Similarly, you can ping between other PCs (e.g., from PC2 to PC5) to verify network connective
    
# OUTPUT
<img width="1050" height="1072" alt="image" src="https://github.com/user-attachments/assets/172d39c1-6920-44ed-8539-1390e9fb5dc5" />

<img width="1039" height="1062" alt="image" src="https://github.com/user-attachments/assets/0d07e57b-d82e-436f-9414-0387f675d25f" />


# RESULT:

Thus the computers in multiple networks using Distance Vector Routing


<img width="576" height="365" alt="image" src="https://github.com/user-attachments/assets/f4245c26-a2f8-4621-b317-0a2c8049f764" />
