# Active Directory Lab Deployment

This lab simulates a small enterprise environment using Windows Server 2022, Windows 11, and Debian 12. It is based on academic exercises from WSB University and demonstrates core skills in identity, access, and domain management.

---

## 🧱 Lab Architecture

- **Domain Controller**: Windows Server 2022 (o-zone.internal)
- **Client**: Windows 11 Enterprise (Win11E)
- **Linux Node**: Debian 12 Bookworm (joined to domain)
- **Virtualization**: Hyper-V
- **Network**: Internal + External (NAT + DHCP)

---

## ⚙️ Main Configurations

### 🧑‍💼 Active Directory Setup
- Created domain `o-zone.internal`
- Configured Organizational Units: `Gdańsk`, `Warszawa`, `Polska`
- Users created: Elon Musk, Steve Musk, Tomasz Szkot, etc.
- Groups configured: `pracownicyGdańsk`, `analitycyGdańsk`, `menedzerowieGdańsk`

### 🔐 Group Policy (GPO)
- Created and linked two policies: `Firma`, `OddziałGdańsk`
- Enforced restrictions on user interface, registry, Control Panel, and network settings
- Enabled folder redirection and login scripts
- Disk quotas and software restrictions applied

### 📡 Networking
- Static IP on DC, DHCP for client
- NAT configured for internet access
- Firewall rules updated

### 🐧 Linux Integration
- Debian 12 configured and joined to domain
- Domain account login tested successfully

## 📸 Screenshots

### OU and Users in Active Directory
Shows the Gdańsk organizational unit with created users and groups.
![OU and Users](https://github.com/user-attachments/assets/78944c09-5fc1-4d92-975d-df5454badce7)

---

### Group Membership: Steve Musk
User belongs to `analitycyGdansk` and `Domain Users`.
![Group Membership](https://github.com/user-attachments/assets/cf3e7c9d-d3a1-4e3a-859a-ece02c22d03a)

---

### Linked Group Policy
GPO `OddziałGdańsk` is linked to the `Gdańsk` OU.
![Linked GPO](https://github.com/user-attachments/assets/8be3e782-80ef-49f3-ad45-4c69f9e84090)

---

### Group Policy Applied
CMD disabled via GPO on Windows 11 client.
![Blocked CMD](https://github.com/user-attachments/assets/07149432-e4f4-4809-a574-623e5708fdb2)


---

### Linux Join Confirmation
Debian joined to AD domain `o-zone.internal`.
![Linux Realm List](https://github.com/user-attachments/assets/b4a665cf-70a1-4be9-b78e-46a2acb609c2)


---

## 💬 Notes
This lab was built fully according to the WSB "Systemy operacyjne" course materials. It demonstrates fundamental sysadmin and security configuration tasks relevant to Blue Team and SOC trainee positions.

