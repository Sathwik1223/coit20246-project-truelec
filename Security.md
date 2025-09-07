# Cybersecurity Risk Assessment

## 1. Introduction
A risk assessment was conducted for Truelec's proposed network design to identify key security risks and recommend appropriate mitigation controls. The assessment considered threats across multiple domains, including data, network, and application security.

## 2. Risk Assessment Summary
The assessment identified 10 key risks. The highest risk was determined to be **"Theft of sensitive customer data"** due to a lack of encryption on the primary customer database, with a risk rating of 20 (Likelihood: 4, Impact: 5).

## 3. Recommended Security Controls
For the highest-risk asset, **Customer Database**, the following three controls are recommended:

1.  **Control 1: Implement Encryption at Rest**
    *   **How it reduces risk:** Encrypting the database ensures that even if data is physically or remotely stolen, it cannot be read without the unique encryption key, rendering the data useless to attackers.
    *   **Implementation:** Enable Transparent Data Encryption (TDE) on the SQL database server hosted in the cloud. The encryption keys should be managed using a dedicated key management service.

2.  **Control 2: Enforce Multi-Factor Authentication (MFA)**
    *   **How it reduces risk:** MFA adds a critical second layer of defense beyond passwords. It prevents unauthorized access even if an employee's password is compromised through phishing or theft.
    *   **Implementation:** Configure conditional access policies in Azure Active Directory (or AWS IAM) to require MFA for all user accounts, especially administrative ones that have access to the database management console.

3.  **Control 3: Implement Network Segmentation**
    *   **How it reduces risk:** Segmentation limits an attacker's ability to move laterally through the network after a breach. By isolating the database server in its own secure network segment, access is restricted only to specific application servers that need it, not every device on the network.
    *   **Implementation:** Create a dedicated subnet for database servers within the cloud VPC/VNet. Configure strict Network Access Control Lists (NACLs) and security group rules to only allow inbound traffic from the application servers on the specific database port.

## 4. Supporting Documents
- [Full Risk Assessment Spreadsheet](risk_assessment.xlsx)
- ![Screenshot of TVAMatrix](images/tva_matrix.png)
