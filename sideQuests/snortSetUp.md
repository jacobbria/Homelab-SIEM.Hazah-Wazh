<div align="center">
  <img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/dc910c3d-7ac0-40c6-ba29-db419d9a0c94" />
  <h1>
    3 Little Piggies: Snort Set-up
  </h1>
</div>

Snort is an open-source Intrusion Detection System (IDS) which I found useful in my <a href="https://github.com/jacobbria/Homelab-SIEM.Hazah-Wazh/tree/main">Wazuh Homelab</a>.
I need a way to detect port scans from Nnamp and send alerts to my endpoints SIEM Manager. So, this side quest had 3 goals - the  3 little piggies
 <div align="center">
  <h3>🐷 Install & Configure Snort of Windows 11 Agent</h3>
  <h3>🐷 Detect Nmap port scans</h3>
  <h3>🐷 Pass logs to Wazuh for detection </h3>
 </div>

This <a href="https://www.youtube.com/watch?v=RwWM0srLSg0&list=PLO0SXQmz3ypmofNFSPnRR7JbJmwvJPSWM&index=2")>video</a> by Steve Gantz was followed for this set-up.
