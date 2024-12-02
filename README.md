# Introduction
This activity simulates an IT Support ticket submitted by a user. Your task is to resolve the issue and document the process, as you would using a ticketing system.  
To troubleshoot this ticket, you will need to import and launch a Virtual Machine named Ticket #1005 using VirtualBox.

# Objectives
Resolve ticket #1005 and document the process.
Equipment/Requirements
Computer with internet connection and VirtualBox installed.
The Ticket #1005 VM (Open Virtual Appliance (OVA) file).


Ticket ID #
1005
User Name
Learner01
User’s email
learner01@TechSolutions.com
Priority
High
Category
Other
Status
Resolved
Subject
Skype is not working
Asset
capstone120
Assigned to
Gregg Nicholas
Description
Hello,

I need to use Skype for a meeting. I powered my computer on and launched Skype, but it just hangs there with that spinning thing spinning forever. Or, it will say “Unable to sign in, please check your internet connection”
It never did this before.
Please help.

Thank you,
Learner01
# Tasks
Upon discovering that the device was unable to obtain an IP address and showed an APIPA (169.x.x.x) address under IPv4, I first checked the network settings to ensure DHCP and DNS were set to automatic. For good measure, I switched the settings to manual and then back to automatic, but this did not resolve the issue. I ran ipconfig /all in Command Prompt, which confirmed the APIPA address and indicated that the device could not reach the DHCP server. To troubleshoot further, I consulted ChatGPT for the appropriate commands to verify and restart the DHCP service. Following the guidance, I opened Command Prompt in administrator mode and ran sc config Dhcp start= auto to ensure the DHCP service was configured to start automatically. I then executed net start Dhcp to start the service and followed up with ipconfig /renew to request a new IP address. These steps resolved the issue, and I verified connectivity by browsing various websites and logging into Skype. Case closed.





# Resolution (Internal-facing)

The issue started when the device showed an APIPA (Automatic Private IP Address) in the ipconfig /all output, meaning it wasn’t able to connect to the DHCP server to get an IP address. I began by double-checking that both DHCP and DNS were set to automatic in the network settings. For good measure, I tried switching these settings to manual and then back to automatic, but no luck.
After looking into it a bit more, I found some steps to make sure the DHCP service was set to start automatically. I opened Command Prompt as admin and ran these commands: sc config Dhcp start= auto to set DHCP to start automatically, net start Dhcp to get it running immediately, and ipconfig /renew to request a new IP from the DHCP server.
That did the trick—once the device got its IP address, I was able to confirm everything was working by browsing some websites and logging into Skype. 



# Resolution (Client-facing)
Hello Learner01,
Your issue has been resolved. The problem was that the device was not able to reach the DHCP server to obtain an IP address, which caused connectivity issues. I made sure that the DHCP service was set to start automatically and manually restarted it. After doing this, the device successfully reconnected to the network, allowing you to browse websites and access Skype without issues.
Please let me know if you need any further assistance.

Best regards,
Gregg Nicholas

IT Support Specialist 

![Identify no network connectivity](https://github.com/GreggNicholas/Ticket-1005-Skype-is-not-working/blob/main/Screen%20Shot%202024-12-01%20at%2022.48.46%20PM.png?raw=true)

![Verifying network & Zoom connectivity](https://github.com/GreggNicholas/Ticket-1005-Skype-is-not-working/blob/main/Screen%20Shot%202024-12-01%20at%2022.49.11%20PM.png?raw=true)





