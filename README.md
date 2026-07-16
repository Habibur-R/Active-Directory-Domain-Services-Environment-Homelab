# Active-Directory-Domain-Services-Environment-Homelab
## Understanding of Active Directory Domain Services by simulating a business environment## 

The aim of this project is to gain a working understanding of Active Directory Domain Services by simulating a business environment with the resources at hand.

The project itself was carried out on a Linux virtualisation server utilising QEMU/KVM and virt-manager to run virtual machines that would be used to host the individual components of the active directory environment. This Linux server ran on a Lenovo think centre M920Q with 64GB RAM, 1TB storage and an intel i7-8700K with 6 cores and 12 threads.

The active directory environment consists of a primary domain controller for centralised management, a secondary domain controller for redundancy, a file server for dedicated file sharing and three computers for 3 users, two of which act as department heads, both R&D and Marketing, within separate organisational units and another acting as a marketing executive within the marketing department. 

When configuring each component of the active directory environment I made sure to assign static IP addresses for each, while pointing the preferred DNS addresses as the static IP address of the domain controller, with the preferred DNS of the domain controller being the secondary domain controller. The secondary preferred DNS address of each component being a loop-back address.

The decision to create an organisational unit comprising of separate departments was made to group departments by function. When establishing group policy, permissions and resource visibility were automated and depended on whether users were managerial or non-managerial staff. This made it easier to provide access to resources required of them through the file server such as performance review templates and sales account information.

This was also done following zero trust principals providing users with the minimum access necessary to carry out tasks required of them.

When configuring the file server administrative privileges were given to allow for the management of files and resources directly from the file server, such as the creation, amendment and assignment of files.
