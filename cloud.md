# Cloud Services Analysis for Truelec

## 1. Requirement Analysis
Truelec currently hosts its booking application on aging on-premise servers. The requirement is to replace:
- **3 servers** at the Melbourne Headquarters
- **1 server** at each of the 3 branch offices (Brisbane, Perth, Adelaide)
- **Total Cloud VMs Required:** 6

## 2. Cloud Virtual Machine Configuration
To ensure a fair comparison, identical specifications were chosen for both cloud providers:

- **vCPUs:** 4
- **RAM:** 16 GB
- **Storage:** 256 GB SSD
- **Operating System:** Windows Server
- **Region:** Australia East / Asia Pacific (Sydney)

## 3. Cost Comparison

### 3.1 Microsoft Azure
- **Cost for one VM per month:** $208.61
- **Cost for 6 VMs per month:** $208.61 * 6 = $1,251.66
- **Total 5-Year Cost (6 VMs):** $1,251.66 * 12 months * 5 years = **$75,099.60**

### 3.2 Amazon Web Services (AWS)
- **Cost for one VM per month:** $155.54
- **Cost for 6 VMs per month:** $155.54 * 6 = $933.24
- **Total 5-Year Cost (6 VMs):** $933.24 * 12 * 5 = **$55,994.40**

## 4. Recommendation
We recommend **Amazon Web Services (AWS)** for Truelec's cloud migration.

**Primary Reason:** Cost-effectiveness. AWS provides a significantly lower total cost of ownership over a 5-year period, saving the company approximately **$19,105** compared to Azure for equivalent performance.

## 5. Advantages and Disadvantages of Cloud vs. On-Premise

### Advantages of Cloud:
- **No Upfront Capital Cost:** No large initial investment in physical hardware.
- **Scalability:** VMs can be resized or added in minutes to meet demand.
- **Maintenance:** The cloud provider handles all hardware maintenance and security updates.
- **Disaster Recovery:** Built-in backup and geographic redundancy options.

### Disadvantages of Cloud:
- **Ongoing Operational Cost:** Costs accumulate continuously.
- **Internet Dependency:** Requires a stable, high-speed internet connection for access.
- **Less Physical Control:** Data is stored off-site on the provider's infrastructure.

## 6. Supporting Documents
- [Azure Price Estimate](quotes/azure_quote.csv)
- [AWS Price Estimate](quotes/aws_vm_quote.xlsx)
