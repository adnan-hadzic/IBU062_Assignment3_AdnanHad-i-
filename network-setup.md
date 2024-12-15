# Network Setup Documentation

## 1. Devices in the Network

### Router
- **Device**: Cisco 1941 Router  
- **Interface IPs**:
  - GigabitEthernet0/0: 168.90.0.1  
  - GigabitEthernet0/1: 210.3.14.1  

### Switches
- **Device**: Cisco 2960-24TT Switch  
- **Switch0**: Connected to PCs, Laptop, and Server  
- **Switch1**: Connected to Servers and a PC  

### Hosts
| Device      | IP Address   | Default Gateway |
|-------------|--------------|-----------------|
| **PC0**     | 168.90.0.2   | 168.90.0.1      |
| **PC1**     | 168.90.0.3   | 168.90.0.1      |
| **Laptop0** | 168.90.0.4   | 168.90.0.1      |
| **Server0** | 168.90.0.5   | 168.90.0.1      |
| **PC3**     | DHCP         | 168.90.0.1      |
| **Server1** | 210.3.14.2   | 210.3.14.1      |
| **PC2**     | 210.3.14.3   | 210.3.14.1      |
| **Server2** | 210.3.14.4   | 210.3.14.1      |
| **PC4**     | DHCP         | 210.3.14.1      |

---

## 2. Packet Tracer File
The network configuration is saved in the **Packet Tracer file**:  
`Task1_NetworkConfig.pkt`

---

## 3. Screenshots of Ping Tool Results
A folder named `screenshots` contains the following images:
1. `ping_laptop_to_server1.png` – Ping result from Laptop0 (168.90.0.4) to Server1 (210.3.14.2).
2. `ping_server1_to_laptop.png` – Ping result from Server1 (210.3.14.2) to Laptop0 (168.90.0.4).

---

## 4. DHCP Configuration Details

### Commands Used on the Router
The following commands were used to configure DHCP on the router:

1. **Access Global Configuration Mode**:
   ```plaintext
   Router> enable
   Router# configure terminal


2. * Configure DHCP for the First Switch*:

Define the DHCP pool for 168.90.0.0/16:
ip dhcp pool FIRST-SWITCH
network 168.90.0.0 255.255.0.0
default-router 168.90.0.1
exit

Exclude router IP:
ip dhcp excluded-address 168.90.0.1

3. ### Configure DHCP for the Second Switch:

Define the DHCP pool for 210.3.14.0/24:
ip dhcp pool SECOND-SWITCH
network 210.3.14.0 255.255.255.0
default-router 210.3.14.1
exit

Exclude router IP:
ip dhcp excluded-address 210.3.14.1

4. ### Verify DHCP Configuration:
show ip dhcp pool
show running-config

5. Ping Test Results
Laptop0 to Server1: Success ✔
Server1 to Laptop0: Partial success (25% packet loss) ✔

End of Document
