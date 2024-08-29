🚀 Personal Webserver on My Old PC
I’m thrilled to share that I’ve successfully transformed my old PC into a personal web server with a custom domain (rjaswal1634.tech). This project has been a long-standing vision of mine, inspired by what I learned about Apache in my CS455 class. The idea was to create a cost-effective, self-hosted server, and after a month of hard work, it's finally a reality!

Project Overview
This repository documents my journey of setting up a personal web server on an old PC, complete with a custom domain, SSL, and Cloudflare integration. Below, I’ll walk you through the challenges I faced, the solutions I discovered, and the key learnings from this experience.

Challenges & Solutions
1. Hardware and Linux Issues
Issue: The journey began with a frustrating boot loop (initramfs error) on Linux.
Solution: After numerous re-installations of different Linux distros (Kali Linux, Red Hat Enterprise Linux, and Ubuntu), I identified the issue as faulty DDR3 memory. Replacing the memory resolved the boot loop.
2. XRDP Configuration
Issue: XRDP caused the server to go into a boot loop, disconnecting the remote desktop connection.
Solution: I explored alternative remote desktop services like VNC. Eventually, I configured XRDP correctly and now use it to access the server from my Windows laptop.
3. Domain Verification Issues
Issue: I had difficulty verifying my domain from get.tech due to missing verification emails.
Solution: The problem was traced back to a Barracuda spam filter set by my school. I manually edited the spam filter list, allowing the verification email to arrive, enabling me to change the nameservers.
4. Connecting with Cloudflare
Issue: Learning how to connect my Cloudflare account with my public IP was challenging, especially regarding port forwarding.
Solution: I delved into networking concepts like network structures, IP addresses, and port forwarding rules to properly configure the connection.
5. Origin Server and SSL Configuration
Issue: Securing the website with SSL and HTTPS required installing an origin server certificate using Cloudflare and Python3 Certbot, complicated by incorrect port forwarding.
Solution: I corrected the port forwarding settings on my router, ensuring port 80 handled HTTP traffic and port 443 handled HTTPS. Additionally, I realized I was editing the wrong config files—corrected by editing the SSL config file for port 443 and the HTTP config file for port 80.
Key Learnings
Technologies & Skills: Apache, Network Structures, Networking Devices, Infrastructure Building, Mail Forwarding, Bash, and Linux terminal commands.
Networking: Gained a deeper understanding of port forwarding, DNS management, and SSL/TLS security.
Problem-Solving: The project required persistence and adaptability, overcoming various hardware and software challenges.
