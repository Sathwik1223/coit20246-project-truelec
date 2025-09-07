# Network Design for Truelec

## 1. Assumptions
- **Headquarters Location:** Melbourne, VIC
- **Headquarters Staff:** 68
- **Branch Office Location (for this design):** Brisbane, QLD
- **Branch Office Staff:** 24

## 2. Network Diagrams
Below are the proposed network designs for the new Truelec offices.

### 2.1 Melbourne Headquarters Network
![Melbourne HQ Network Diagram](images/network_hq.png)

### 2.2 Brisbane Branch Office Network
![Brisbane Branch Network Diagram](images/network_branch.png)

## 3. Key Design Decisions
We designed the network for reliability, security, and future growth.

- **Redundancy:** The HQ design includes a redundant internet connection from a second ISP. This provides automatic failover if the primary connection fails, ensuring continuous availability for critical services like the CRM and accounting software.
- **Scalability:** We used a core Layer 3 switch in Melbourne. This allows us to create logical networks (VLANs) for different departments (e.g., HR, Projects, Finance) which improves security and performance. It also makes it easy to add more switches and users in the future without redesigning the entire network.
- **WiFi Design:** For both offices, we recommend multiple WiFi 6 Access Points (APs) placed strategically to avoid dead zones.
    - **SSID (Network Name):** `Truelec-Corporate`
    - **Security:** WPA3-Enterprise (This requires a separate authentication server for the highest security)
    - **Band:** Dual-band (2.4GHz for legacy devices, 5GHz for high-speed access)
    - **Guest Network:** A separate guest network with a different SSID (`Truelec-Guest`) will be implemented to keep visitor traffic isolated from the main corporate network.

## 4. IP Addressing Scheme
Based on our student IDs (12313788 -> **88**, 12315744 -> **44**), we used the following IP ranges:

- **Melbourne HQ Network:** `88.1.0.0/16`
- **Brisbane Branch Network:** `44.1.0.0/16`

The `/16` mask provides a very large number of addresses (over 65,000) for each location, which is more than enough for all current devices and plenty for future expansion.

## 5. Recommended Hardware
We recommend the following equipment for a reliable and secure network:

| Device | Model | Approx. Price (AUD) | Justification |
| :--- | :--- | :--- | :--- |
| **Core Router** | Cisco ISR 1100 Series | $1,500 | Reliable and capable of handling VPN connections to all branch offices. |
| **Layer 3 Switch** | Cisco Catalyst 9200 Series (48-port) | $4,000 | Provides the switching capacity and VLAN capabilities needed for the HQ's 68 users. |
| **Wireless AP** | Cisco Catalyst 9100ax WiFi 6 AP | $1,800 | High-performance, business-grade access points that support many concurrent users. |
| **Firewall** | FortiGate 60F | $700 | A strong firewall with advanced security features to protect against cyber threats. |
| **Branch Router** | Ubiquiti Dream Machine | $500 | An all-in-one device suitable for the smaller Brisbane branch, combining a router, switch, and firewall. |

*Note: Prices are estimates from quick online searches. Final pricing may vary.*

## 6. Task Allocation
- **Sathwik Bongoni:** Primary designer of the network topology diagrams and IP addressing scheme.
- **Mallala Sai Deekshith:** Primary researcher for hardware recommendations and specifications. Collaborated on design decisions.
