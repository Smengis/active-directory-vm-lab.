# active-directory-vm-lab

This project documents my hands-on experience deploying and configuring **Active Directory Domain Services (AD DS)** within a **Windows Server virtual machine environment hosted on AWS**.

---

## 🎯 Objective

Build and configure a functional Active Directory domain by installing AD DS, promoting a Windows Server to a Domain Controller, and managing directory objects such as users, groups, and Organizational Units (OUs).

---

## 🧠 Skills Demonstrated

- Installing and configuring Active Directory Domain Services (AD DS)
- Promoting a Windows Server to a Domain Controller
- Creating and managing a new forest and domain
- Structuring Organizational Units (OUs)
- Managing users and groups using Active Directory Users and Computers (ADUC)
- Understanding domain-based authentication and access control

---

## 🛠 Tools & Technologies

- Windows Server (AWS EC2 AMI)
- Active Directory Domain Services (AD DS)
- Active Directory Users and Computers (ADUC)
- Server Manager
- Amazon EC2 (Virtual Machine)

---

## 📋 Lab Overview

This lab was completed in a virtualized AWS EC2 environment to simulate a real-world Windows domain infrastructure.  
The focus was on centralized identity management, authentication, and directory services.

---

## 🚀 Steps Performed

1. Deployed a Windows Server instance on AWS EC2  
2. Configured initial server settings (hostname and networking)  
3. Installed the Active Directory Domain Services (AD DS) role  
4. Promoted the server to a Domain Controller  
5. Created a new forest and domain  
6. Verified domain functionality  
7. Created and managed Organizational Units (OUs)  
8. Added and managed user and group accounts using ADUC  
9. Each step was validated to ensure proper domain functionality before proceeding to the next phase.

---

## 📸 Screenshots

Screenshots are included below to document each major stage of the configuration process.

---

## 📚 What I Learned

This lab strengthened my understanding of how Active Directory is deployed and managed in enterprise environments and reinforced best practices for centralized identity and access management.

---

## 🔮 Next Steps

- Join a client machine to the domain  
- Implement Group Policy Objects (GPOs)  
- Expand the lab with additional users, groups, and security policies  
## 📸 Screenshots & Explanations

### Screenshot 1: Active Directory Domain Services and DNS Installed
**Description:**  
This screenshot shows **Active Directory Domain Services (AD DS)** and **DNS Server** successfully installed using the *Add Roles and Features Wizard* in Server Manager.
<img width="1440" height="900" alt="Screenshot 2026-01-12 at 8 21 50 AM" src="https://github.com/user-attachments/assets/12d7219b-88eb-4844-a995-52b694e3e6de" />

**Why this matters:**  
AD DS relies on DNS for name resolution. Having both roles installed confirms the server is properly prepared to function as a Domain Controller.

**What this verifies:**
- AD DS role installation completed successfully
- DNS Server role installed to support domain services
- Server is ready for domain controller promotion

---

### Screenshot 2: Server Manager Dashboard – Domain Controller Verification
**Description:**  
This screenshot displays the Server Manager dashboard with **AD DS** and **DNS** roles active and manageable.
![IMG_9929](https://github.com/user-attachments/assets/afd3664f-e06c-4b85-8ca8-71ae7b0538ab)

**Why this matters:**  
This confirms that post-deployment configuration was completed and the server was successfully promoted to a **Domain Controller**.

**What this verifies:**
- Domain Controller promotion succeeded
- Core Active Directory services are running
- The environment is operational and manageable

---

### Screenshot 3: Active Directory Users and Computers – Object Creation
**Description:**  
This screenshot shows the **Active Directory Users and Computers (ADUC)** console with a **Security Group** being created inside the domain.
<img width="1440" height="900" alt="Screenshot 2026-01-12 at 8 34 13 AM" src="https://github.com/user-attachments/assets/40835f69-6b26-4369-b126-5a1a24950399" />

**Why this matters:**  
Creating directory objects is only possible after a domain has been created, DNS is functioning, and Active Directory is fully operational.

**What this verifies:**
- The Active Directory domain (`skool.local`) exists
- The domain is writable and functioning correctly
- Administrative tools can successfully manage directory objects


---

### 📝 Note on Domain Naming
The domain name (`skool.local`) was configured during the Domain Controller promotion process.  
Although the domain-naming wizard screen was not captured at the time, successful configuration is verified by:
- The presence of the `skool.local` domain in Active Directory Users and Computers
- Successful creation of directory objects within the domain

This approach aligns with real-world enterprise documentation practices, where **validation and verification** are prioritized over capturing every installation wizard step.

---

### ✅ Outcome
Successfully deployed and validated an Active Directory Domain Controller with DNS integration, confirming the environment is fully operational.
