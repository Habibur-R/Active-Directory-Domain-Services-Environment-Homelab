# Active-Directory-Domain-Services-Environment-Homelab
## Understanding of Active Directory Domain Services by simulating a business environment ## 

The aim of this project is to gain a working understanding of Active Directory Domain Services by simulating a business environment with the resources at hand.

The project itself was carried out on a Linux virtualisation server utilising QEMU/KVM and virt-manager to run virtual machines that would be used to host the individual components of the active directory environment. This Linux server ran on a Lenovo think centre M920Q with 64GB RAM, 1TB storage and an intel i7-8700K with 6 cores and 12 threads.

<img width="2086" height="1214" alt="Screenshot From 2026-07-16 23-50-08" src="https://github.com/user-attachments/assets/c453954b-5ed6-4e47-a671-52f81885c3f2" />

The active directory environment consists of a primary domain controller for centralised management, a secondary domain controller for redundancy, a file server for dedicated file sharing and three computers for 3 users, two of which act as department heads, both R&D and Marketing, within separate organisational units and another acting as a marketing executive within the marketing department. 

When configuring each component of the active directory environment I made sure to assign static IP addresses for each, while pointing the preferred DNS addresses as the static IP address of the domain controller, with the preferred DNS of the domain controller being the secondary domain controller. The secondary preferred DNS address of each component being a loop-back address.

The decision to create an organisational unit comprising of separate departments was made to group departments by function. When establishing group policy, permissions and resource visibility were automated and depended on whether users were managerial or non-managerial staff. This made it easier to provide access to resources required of them through the file server such as performance review templates and sales account information.

This was also done following zero trust principals providing users with the minimum access necessary to carry out tasks required of them.

When configuring the file server administrative privileges were given to allow for the management of files and resources directly from the file server, such as the creation, amendment and assignment of files.

<img width="2560" height="1440" alt="Screenshot From 2026-05-14 23-09-35" src="https://github.com/user-attachments/assets/24c2cd6d-4933-4a06-8a04-48e0379f4b6b" /> 

<img width="1740" height="1220" alt="Screenshot From 2026-05-19 16-32-59" src="https://github.com/user-attachments/assets/2481c648-ccc5-4767-9a05-9ccd31a2ed69" />

<img width="1740" height="1220" alt="Screenshot From 2026-05-19 17-33-17" src="https://github.com/user-attachments/assets/4d826730-9635-4c7b-8e22-0bec97b7cb7c" />

<img width="1740" height="1220" alt="Screenshot From 2026-05-19 18-31-47" src="https://github.com/user-attachments/assets/90ec49a4-a344-430e-b488-136ade7a160f" />

<img width="1258" height="868" alt="Screenshot From 2026-06-13 15-40-59" src="https://github.com/user-attachments/assets/b58a4708-23ee-4d3b-99e3-557c52422787" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-07-54" src="https://github.com/user-attachments/assets/13b550b3-2c96-4e0c-90b2-e03518e4440e" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-10-58" src="https://github.com/user-attachments/assets/e273b4d3-e3fa-492e-a817-0be27c35802a" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-12-20" src="https://github.com/user-attachments/assets/ba23fbc6-4e4e-4dc3-858b-d24c2d4888fa" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-14-43" src="https://github.com/user-attachments/assets/84b948ab-d0fb-411b-8aa0-789642ffcbf5" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-17-07" src="https://github.com/user-attachments/assets/05cce4a5-acdf-4d34-9ee5-16c429501f4a" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-22-40" src="https://github.com/user-attachments/assets/dad135cd-0b38-470e-80ee-20fcb260d80e" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-24-54" src="https://github.com/user-attachments/assets/a7bb97f3-dbd2-4341-a467-b61bb4bc1973" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-25-53" src="https://github.com/user-attachments/assets/06a7c9eb-1d79-440a-b99e-f387943d79bd" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-32-37" src="https://github.com/user-attachments/assets/94496c80-9bdd-40a2-b89a-8034e33d70f4" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-32-56" src="https://github.com/user-attachments/assets/4e803b99-4e97-4781-8720-d0a1ebc252f2" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-38-45" src="https://github.com/user-attachments/assets/6de647ad-c345-48ad-b809-638cd384ce1d" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-39-01" src="https://github.com/user-attachments/assets/3b2671d2-dfbf-4232-8109-fde6fde26cd1" />

<img width="1738" height="1120" alt="Screenshot From 2026-07-16 23-39-16" src="https://github.com/user-attachments/assets/73dd0466-fa0f-4aa8-9762-e70e87e01e7f" />

<img width="2086" height="1214" alt="Screenshot From 2026-07-16 23-46-10" src="https://github.com/user-attachments/assets/e183afe9-654e-43a8-8fde-fca0db4e1729" />

