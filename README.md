# Microsoft-Sentinel-Tutorial-with-Heatmap-Showing-Live-RDP-Brute-Force-Attacks

Based on Video Created By: Josh Madakor - https://www.youtube.com/watch?v=RoZeVbbZ0o0

Created By: Jose Romero

Lab Overview:

The objective of this lab is to set up Microsoft Sentinel, a cloud-based Security Information and Event Management (SIEM) system. Additionally, a virtual machine will be created in the cloud and configured as a honeypot, intentionally made highly vulnerable to the internet. This setup will allow monitoring and logging of various attacks originating from diverse IP addresses worldwide. The ultimate goal is to create a geographical map displaying the origins of these attacks.

Technologies and Protocols Used:

•	Microsoft Azure - Microsoft's public cloud computing platform. It provides a broad range of cloud services, including computing, analytics, storage, and networking. Users can choose from these services to develop and scale new applications or run existing applications in the public cloud.

•	Services within Azure: 

Log Analytics Workspace - a logical storage unit in Azure where all log data generated by Azure Monitors are stored.

Sentinel (Microsoft’s SIEM) - is a cloud-native security information and event management (SIEM) platform that uses built-in AI to help analyze large volumes of data across an enterprise

•	PowerShell – is a task automation and configuration management program from Microsoft, consisting of a command-line shell and the associated scripting language.

•	Remote desktop protocol - is a secure, interoperable protocol that creates secure connections between clients, servers, and virtual machines.

Overview of technical steps: 

The process begins by setting up an Azure subscription, which offers $200 worth of free credits. Next, the objective is to create a virtual machine within Azure and disable the external firewall and the Windows firewall. This step, though unconventional for ensuring security, is aimed at deliberately exposing the virtual machine to the internet, making it an attractive target for potential attackers. This approach will aid in swiftly gathering data on intrusion attempts from various sources.

Following this, a log repository will be created in Azure, known as a Log Analytics Workspace. This workspace will serve as a centralized hub for ingesting and storing logs generated by the vulnerable virtual machine. To enhance cybersecurity efforts, Microsoft Sentinel will be set up. With Microsoft Sentinel, a visual map will be created to illustrate the origin and characteristics of these intrusion attempts, aiding in identifying the geographic locations and other relevant details about the attackers.

As part of the strategy, PowerShell will be utilized in this lab. The primary motivation behind this choice is that typically when a login attempt fails on a Windows machine, limited information about the source of the attack is received. However, the intention is to go further by using PowerShell to extract the IP address from the Windows logs and transmit this information to a third-party API. This API will enrich the data by providing latitude, longitude, and additional geographical information, such as the country and state or province. The processed data will be sent back to the virtual machine to create custom logs that include this valuable geographic information.


Step-by-step overview of the lab:

1.	Create an Azure subscription, which includes free $200 credits for use.
2.	Set up a virtual machine in Azure named "honeypot-vm" and disable external and Windows firewalls, making it a target for potential RDP brute force attacks.
3.	Utilize a PowerShell script to extract the IP addresses of attackers attempting to compromise the "honeypot-vm." Send these IP addresses to a third-party API to retrieve specific location information.
4.	Establish a log repository in Azure known as a Log Analytics Workspace, which will serve as a centralized hub for ingesting and storing logs generated by "honeypot-vm."
5.	Configure Microsoft Sentinel to gain insights into intrusion attempts. Create visual maps that display the origin and characteristics of these attacks, allowing the identification of the geographic locations and other relevant details of the attackers.

To view the full file with instructions and photos go to the pdf file 

To view hyperlinks from the pdf file go to the Links folder
