# Version 1.1
## New Features
- Tested on Centos 8.1 with OpenJDK. 
- The Name of the ipquorum service can now be changed to have custom name or run several services running on same VM. **ipquorum_service_name: ipquorum**
- Able to run several services on same VM/Host by changing the variable **ipquorum_service_name: ipquorum**
- Able to change the work directory for the service, ip-quorum.jar file and logs are located default in /opt/IBM **ipquorum_service_path: /opt/IBM**
- sshpass is default checking ssh identity and need to be added to known-hosts. by using **stricthostkeycheking=false** it will accept automatic the ssh identity.
- Added check for epel repo, this is needed for Centos8/rhel8
- Dynamic motd/banner, changes after the ipquorum name. 
- Added check for package manager DNF that is going to replace YUM and is default in Centos 8.1
- Added 5 retries on the package installer from DNF/YUM. 
- Added Release Notes


## Limitation 
 - Banner/Motd will update after latest Ansible run: **ipquorum_service_name: ipquorum** so if there is several ipquorum services, it will not append all services in the motd. 



# Version 1.0

## Features

- **Creates IP-Quorum Service, (So it starts and stops with host)**
- **Copy inn IP-Quorum.jar file from local folder**
- **Creates Banner with IP-Quorum Service Information**
- **Disables or Create Firewalld rules.**
- **Check and disabled selinux**
- **Create new IP-Quorum app file directly from SV node (Requires Repo)**
    - Connects to SV nodes and Generate new IP-Quorum app file
    - Copy inn new IP-Quorum app directly from SV nodes
- **Installation of Supported Java**
     - OpenJDK (Requires Repo)
     - Java IBM (Local Install files or url)
     - JavaSDK Oracle (Local Install files or url)