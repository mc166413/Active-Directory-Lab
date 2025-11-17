# Active Directory Home Lab – lab.local

Fully functional AD DS lab built from scratch in VirtualBox (Host-Only networking).

## What I Built
- Windows Server 2022 Domain Controller (DC02)
- New forest: **lab.local**
- Proper OU structure + domain user (john.doe)
- Windows 10 client cleanly joined to the domain
- Group Policy enforcement (forced desktop wallpaper)

## Proof Screenshots (November 16, 2025)

1. **Client login screen showing only the domain user**  
   `LAB\john.doe` is the sole account presented – proof of successful domain join and profile caching.

2. **System Properties confirming domain membership**  
   Full computer name `WIN10-CLIENT.lab.local` and Domain: `lab.local`.

3. **gpresult /r as john.doe**  
   Shows the client is receiving and applying domain Group Policy Objects.

4. **AD DS role installed on DC02**  
   Server Manager confirmation that Active Directory Domain Services is active.

5. **Get-ADDomain PowerShell output**  
   Verifies `lab.local` forest and domain are fully operational.

6. **ADUC – OU structure and domain user**  
   Employees OU containing user `john.doe` with correct attributes.

7. **DNS forward lookup zone (lab.local)**  
   Contains proper A records for both DC02 and WIN10-CLIENT – proves integrated DNS is working.

8. **Forced desktop wallpaper GPO applied**  
   User Configuration GPO successfully enforced (appears black due to known VirtualBox guest driver behavior – still 100 % confirmation the GPO was processed).

These 8 screenshots fully demonstrate DC promotion, DNS integration, domain join, user creation, and Group Policy enforcement end-to-end.

## Skills Demonstrated
- AD DS installation & dcpromo
- DNS integration
- OU design & user creation
- Group Policy creation, linking, and enforcement
- Domain join & troubleshooting

Built 100% from scratch.

Ready for junior sysadmin / IT support roles.

Feel free to reach out – happy to walk through any part live!
