<div align="center">

  ## Initial Set-up

| Resources Used |
|----------|
| [Wazuh Documentation](https://documentation.wazuh.com/current/quickstart.html) |
| [Setup Your Own FREE SIEM at Home! - Wazuh (YouTube)](https://youtu.be/bltbJ2TUQWU?si=L07PNs15z8w26U6v) |
| Gemini or ChatGPT (for basic scripts I didn’t know) |
| Google, Google, and some more Google! |
## Wazuh Server Set-Up

<table>
<tr>
  <td>

### Wazuh Server Set-Up

| *Component*       | Specification |
|-------------------|---------------|
| *Operating System*| Ubuntu        |
| *Disk (Storage)*  | 50 GB         |
| *RAM*             | 8 GB          |
| *Virtualization*  | VirtualBox    |

  </td>
  <td>

### Wazuh Agent Set-Up

| *Component*       | Specification |
|-------------------|---------------|
| *Operating System*| Windows 11    |
| *Disk (Storage)*  | 1 TB          |
| *RAM*             | 16 GB         |

  </td>
</tr>
</table>


</div>
&emsp;The memory is pretty low and not what I would recommned for future projects. However, the host
machine is a laptop with limited memory and I didnt intend for large amounts of logs to be stored.
It will do!


&emsp;All things considered setting up the arichtecture wasnt too bad but it did require some 
troubleshooting. Wazuh server gave me several issues when downloading and I didn't find
their error messages very helpful. The final working solution appeared to be giving it
more memory - ramping up from 30GB to 50GB- but I'm hesitant to declare that a 
consistent solution.

&emsp;Agent installation on the Windows machine was easy - configuation wasn't as smooth. 
Wazuh makes it easy to get an agent deployed with it's "follow-along" process at the initial
dashboard. It will point the agent to server and provide you with the needed commands. 

  I had to dig in to some configuration files on my agent to get machines to talk. They were able to ping
each other so the issue was pointing to agent to the server in the ossec.conf file. After which - Hazzuh!
My server sees and receives from the agent.
