# Active-Directory-Domain-Services-Environment-Homelab
## Understanding Active Directory Domain Services by simulating a business environment ## 

### Overview ###
The aim of this project is to gain a working understanding of Active Directory Domain Services by simulating a business environment.

The active directory environment consists of a primary domain controller for centralised management, a secondary domain controller for redundancy, a file server for dedicated file sharing and three computers for 3 users, two of which act as department heads, both R&D and Marketing, within separate organisational units and another acting as a marketing executive within the marketing department. 

When configuring each component of the active directory environment I made sure to assign static IP addresses for each, while pointing the preferred DNS addresses as the static IP address of the domain controller, with the preferred DNS of the domain controller being the secondary domain controller. The secondary preferred DNS address of each component being a loop-back address.

The decision to create an organisational unit comprising of separate departments was made to group departments by function. Similiarily group policy and security groups were established depending on department, allowing access to shared files and resources through the file server such as sales account data as an executive.

This was done using explicit permissions such as read only or read and write permissions being specified.

The project itself was carried out on a Linux virtualisation server utilising QEMU/KVM and virt-manager to run virtual machines that would be used to host the individual components of the active directory environment. This Linux server ran on a Lenovo Think Centre M920q with 64GB RAM, 1TB storage and an intel i7-8700K with 6 cores and 12 threads.

<img width="2086" height="1214" alt="Screenshot From 2026-07-16 23-50-08" src="https://github.com/user-attachments/assets/c453954b-5ed6-4e47-a671-52f81885c3f2" />

Installed and set-up windows server ISO, installed active directory domain services, established a domain, promoted server to domain controller, assigned static IP and preferred DNS addresses of the Domain controller:

<img width="2560" height="1440" alt="Screenshot From 2026-05-14 23-09-35" src="https://github.com/user-attachments/assets/24c2cd6d-4933-4a06-8a04-48e0379f4b6b" /> 

<img width="1740" height="1220" alt="Screenshot From 2026-05-19 16-32-59" src="https://github.com/user-attachments/assets/2481c648-ccc5-4767-9a05-9ccd31a2ed69" />

<img width="1740" height="1220" alt="Screenshot From 2026-05-19 17-33-17" src="https://github.com/user-attachments/assets/4d826730-9635-4c7b-8e22-0bec97b7cb7c" />

<img width="1740" height="1220" alt="Screenshot From 2026-05-19 18-31-47" src="https://github.com/user-attachments/assets/90ec49a4-a344-430e-b488-136ade7a160f" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-07-54" src="https://github.com/user-attachments/assets/13b550b3-2c96-4e0c-90b2-e03518e4440e" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-12-20" src="https://github.com/user-attachments/assets/ba23fbc6-4e4e-4dc3-858b-d24c2d4888fa" />

Installed a secondary domain controller and assigned static IP and preferred DNS addresses:

<img width="1734" height="1125" alt="Screenshot From 2026-07-17 16-17-07" src="https://github.com/user-attachments/assets/6c2f3f84-14f6-4bbf-8a01-5195639e8f76" />

<img width="1734" height="1125" alt="Screenshot From 2026-07-17 16-18-34" src="https://github.com/user-attachments/assets/69007057-cee9-4ec6-b9e4-f08459175925" />

Created organisational units, users and established group policy:

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-10-58" src="https://github.com/user-attachments/assets/e273b4d3-e3fa-492e-a817-0be27c35802a" />

<img width="1736" height="1178" alt="Screenshot From 2026-07-17 16-08-27" src="https://github.com/user-attachments/assets/e47831ca-7dc7-4e7a-9dd0-bf001679e9df" />

Configured a windows server and installed the file server role, assigned static IP and preferred DNS addresses, implemented a hard disk image .VHD for the shared drive, created a shared drive, enabled sharing, created folders, files and security groups:

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-14-43" src="https://github.com/user-attachments/assets/84b948ab-d0fb-411b-8aa0-789642ffcbf5" />

<img width="1734" height="1125" alt="Screenshot From 2026-07-17 16-29-42" src="https://github.com/user-attachments/assets/d1bf7876-7d5d-4c58-bc64-04642e3c92a3" />

<img width="1258" height="868" alt="Screenshot From 2026-06-13 15-40-59" src="https://github.com/user-attachments/assets/ebef4a43-2d41-4324-8d2e-fb29d783b5aa" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-24-54" src="https://github.com/user-attachments/assets/a7bb97f3-dbd2-4341-a467-b61bb4bc1973" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-17-07" src="https://github.com/user-attachments/assets/05cce4a5-acdf-4d34-9ee5-16c429501f4a" />

<img width="1734" height="1125" alt="Screenshot From 2026-07-17 16-37-47" src="https://github.com/user-attachments/assets/f7410dde-4579-4689-b198-d09be85f8d0f" />

Installed windows 11 and logged on to the marketing executive user account, joined the Marketing Executive user account to the domain controller, assigned static IP and preferred DNS addresses, mapped network drive to access shared drive, able to access folders and files when permitted, if not permitted an error occurs, the same steps were carried out for the other user accounts:

<img width="2086" height="1214" alt="Screenshot From 2026-07-16 23-46-10" src="https://github.com/user-attachments/assets/e183afe9-654e-43a8-8fde-fca0db4e1729" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-38-45" src="https://github.com/user-attachments/assets/6de647ad-c345-48ad-b809-638cd384ce1d" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-25-53" src="https://github.com/user-attachments/assets/06a7c9eb-1d79-440a-b99e-f387943d79bd" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-39-01" src="https://github.com/user-attachments/assets/3b2671d2-dfbf-4232-8109-fde6fde26cd1" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-39-16" src="https://github.com/user-attachments/assets/73dd0466-fa0f-4aa8-9762-e70e87e01e7f" />
