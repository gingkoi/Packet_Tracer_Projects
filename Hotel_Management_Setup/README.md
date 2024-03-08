Design a modern hotel network. The hotel has three floors. In the first floor, there is three departments (reception, store, logistics). The second floor, three departments (Finance, HR, sales/marketing). Lastly third floor, two departments (IT and Admin).

The following are part of the considerations for design and implementations.

1. There should be three routers connecting each floor (All placed in the server room in IT department)

2. All routers should be connected to each other using serial cable.

3. The network between the routers should be 10.10.10.0/30 , 10.10.10.4/30, 10.10.10.8/30

4. Each floor is expected to have one switch.

5. Each floor should have WiFi networks connected to laptops and phones.

6. Each department should have a printer.

7. Each department should be in different VLANs

1st Floor
- Reception : VLAN 80, Network of 192.168.8.0/24
- Store : VLAN 70, Network of 192.168.7.0/24
- Logistic : VLAN 60, Network of 192.168.6.0/24

2nd Floor
- Finance : VLAN 50, Network of 192.168.5.0/24
- HR : VLAN 40, Network of 192.168.4.0/24
- Sales : VLAN 30, Network of 192.168.3.0/24

3rd Floor
- Admin : VLAN 20, Network of 192.168.2.0/24
- IT : VLAN 10, Network of 192.168.1.0/24

8. Use OSPF as routing protocol for advertise routes.

9. All devices in network is expected obtain IP address dynamically configured as DHCP server.

10. All devices in network is expected to communicate with each other.

11. Configure SSH in all routers for remote login.

12. In IT department, add PC called Test-PC to port fa/01 and use it to test remote login.

13. Configure port security to IT department switch to allow only "Test-PC" to access port fa/01 (Use sticky method to obtain mac-address with violation mode of shutdown).

