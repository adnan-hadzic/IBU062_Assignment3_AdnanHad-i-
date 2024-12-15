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

## 4. DHCP Configuration
- **FIRST-SWITCH Pool**: 168.90.0.0/16  
- **SECOND-SWITCH Pool**: 210.3.14.0/24  
- **Excluded Addresses**:
  - 168.90.0.1  
  - 210.3.14.1  

---

## 5. Ping Test Results
- **Laptop0 to Server1**: Success ✔  
- **Server1 to Laptop0**: Partial success (25% packet loss) ✔  

---

*End of Document*
