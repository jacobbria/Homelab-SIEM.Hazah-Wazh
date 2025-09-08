<div align="center">
  
## LOG GENERATION & ANALYSIS

We have communication between agents and server - lets generate some actions and get the log(s) rolling!
<p align="center">
  <img src="https://media1.tenor.com/m/8SwMrENO6AEAAAAC/pikachu-togepi.gif" width="300" alt="Pikachu Gif">
</p>

</div>
<div align="center">
  <h1> Part 1: Basic Log Generation </h1>
</div>

An easy one to start off with is an incorrect login from the physical device. Lets input the wrong password
about 10 times
<div align="center">
  <img width="882" height="192" alt="image" src="https://github.com/user-attachments/assets/0b45b0e8-c206-4d90-a432-b3893bc27afa" />
</div>

 **TO DO** 
 Insert a screenshot

Wazuh querying is great - it uses a pretty standard format. Having used ServiceNow querying and SQL language before its a breeze!
<div align="center">
  <img width="623" height="268" alt="image" src="https://github.com/user-attachments/assets/9c14c832-ffcb-423c-8c98-fdfde956e877" />
</div>

Now how about showing if someone was trying to access the device <i>internally</i>?  
On the agent machine I started an elevated PowerShell session and ran the *whoami* command.  
<p align="center">
  <img width="291" height="89" alt="image" src="https://github.com/user-attachments/assets/dc00a584-4d67-42ba-9981-665147e87493" />
</p>

On our dashboard we can see a new log was generated detailing the event. Device name,
IP, account name, channel used, and other important information can be found here in either
a table format or the JSON it's sent in.

Also provided is the MITRE techniques and tactics most associated with the log event. 
<p align="center">
  <img width="780" height="125" alt="image" src="https://github.com/user-attachments/assets/119c8b87-bbbb-471d-ac6b-c658a040c5b3" />  
</p>
It aligned perfectly as escalating to a local admin account gives attackers a better foothold to keep going up the chain. I'm just
glad it was a simple *whoami* command. You can read more about the technique [here](https://attack.mitre.org/techniques/T1078/).

<h1 align="center"> Part 2: A Slighly More Sophisticated Attack</h1>
Let's see if we can detect activity in the different stages of the <a href="https://attack.mitre.org/">Cyber Kill-Chain</a>
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/19fdf6c8-6beb-418f-9266-b5dbced142bd" />
