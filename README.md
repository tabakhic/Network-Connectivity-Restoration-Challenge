# 🖧 DHCP Network Troubleshooting Challenge (Cybrary) 

**Objective**: Fix DHCP/DNS issues on Linux-A (192.168.1.0/24) to restore internet access and FILESERVER connectivity.  


![Topology](https://imgur.com/U14X4Km.png)
---

## Solution Steps  

### 1. Configure DHCP Scope on pfSense  
![1.PNG](https://imgur.com/iO5cFSj.png)  
1. **Access Firewall-A**:  
   Navigate to `Services > DHCP Server > LAN`  
2. **Set DHCP Range**:  
   - Enable DHCP server  
   - Range: `192.168.1.100–192.168.1.110`  
3. **Configure DNS**:  
   - Gateway: `192.168.1.1`  
   - DNS Servers: `8.8.8.8` (Google) and `192.168.1.20` (Local DNS)  
4. Save changes and restart DHCP service.  

---

#### 2.PNG: **DNS Server Configuration**  
![DNS Server Configuration](https://imgur.com/119fJuE.png)
*Shows DNS server entries: `8.8.8.8`, `192.168.1.20`, and a third DNS server.*  

---

#### 3.PNG: **pfSense IPsec Status Page**  
![IPsec Status](https://i.imgur.com/PMzEMfy.png)
*Displays pfSense IPsec connection status, including details for "Connection to Site-B".*  

---

#### 4.PNG: **Flag Retrieval Process in Terminal**  
![Flag Script Execution](https://i.imgur.com/Y1cj6og.png) 
*Shows the process of troubleshooting DNS resolution for `FILESERVER`, fixing it via `/etc/hosts`, and retrieving the flag with `./flag.sh`.*  

