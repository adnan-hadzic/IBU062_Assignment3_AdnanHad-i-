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
| Device      | IP Address   |
|-------------|--------------|
| **PC0**     | 168.90.0.2   |
| **PC1**     | 168.90.0.3   |
| **Laptop0** | 168.90.0.4   |
| **Server0** | 168.90.0.5   |
| **Server1** | 210.3.14.2   |
| **PC2**     | 210.3.14.3   |
| **Server2** | 210.3.14.4   |

## 2. Packet Tracer File
The network configuration is saved in the **Packet Tracer file**:  
`Task1_NetworkConfig.pkt`

## 3. Screenshots of Ping Tool Results
A folder named `screenshots` contains the following images:
1. `ping_laptop_to_server1.png` – Ping result from Laptop0 (168.90.0.4) to Server1 (210.3.14.2).
2. `ping_server1_to_laptop.png` – Ping result from Server1 (210.3.14.2) to Laptop0 (168.90.0.4).

---

*End of Document*
