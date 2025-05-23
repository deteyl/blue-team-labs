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

---

## 💬 Notes
This lab was built fully according to the WSB "Systemy operacyjne" course materials. It demonstrates fundamental sysadmin and security configuration tasks relevant to Blue Team and SOC trainee positions.

