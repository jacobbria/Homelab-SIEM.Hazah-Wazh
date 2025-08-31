We have communication between agent and server - lets generate some actions and get the log(s) rolling!

On the agent machine I started an elevated PowerShell session and ran the *whoami* command.  
<img width="291" height="89" alt="image" src="https://github.com/user-attachments/assets/e479f06d-76e6-4d3e-97d8-3ba378b7c515" />  

On our dashboard we can see a new log was generated detailing the event. Device name,
IP, account name, channel used, and other important information can be found here in either
a table format or the JSON it's sent in.

Also provided is the MITRE techniques and tactics most associated with the log event. 
<img width="780" height="125" alt="image" src="https://github.com/user-attachments/assets/119c8b87-bbbb-471d-ac6b-c658a040c5b3" />  
It aligned perfectly as escalating to a local admin account gives attackers a better foothold to keep going up the chain. I'm just
glad it was a simple *whoami* command. You can read more about the technique [here](https://attack.mitre.org/techniques/T1078/).

Lets see how an executable script would perform. From an elevated account we run the script (found here) which should create a folder
and text file inside. 
