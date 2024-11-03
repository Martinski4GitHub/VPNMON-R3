# VPNMON-R3 v1.3.8
## Updated on 2024-Nov-02
## Asus-Merlin VPN Monitor R3

![image](https://github.com/user-attachments/assets/476d3d78-bcc4-482d-ad3f-8b7d75501e58)

**EXECUTIVE SUMMARY:** VPNMON-R3 (vpnmon-r3.sh) is an all-in-one script that is optimized to maintain multiple VPN connections and is able to provide for the capabilities to randomly reconnect using a specified server list containing the servers of your choice. Special care has been taken to ensure that only the VPN connections you want to have monitored are tended to. This script will check the health of up to 5 VPN connections on a regular interval to see if monitored VPN connections are connected, and sends a ping to a host of your choice through each active connection. If it finds that a connection has been lost, it will execute a series of commands that will kill that single VPN client, and randomly picks one of your specified servers to reconnect to for each VPN client. It also monitors your WAN/Dual-WAN connection and drops back until your WAN connection comes back up to reconnect your VPN tunnels.

**FINAL RELEASE NOTES:** Throughout the development of VPNMON-R2, I had many requests from those who were running multiple VPN connections. R2 was designed to support a single VPN connection, and would have been tough to integrate the ability to manage multiple VPN connections within it. I decided it was just better to start from the ground up with R3. Also, I wanted R3 to be a more open platform, that gives you the freedom and ability to use whatever VPN provider you want, without being tied to certain BIG-NAME VPN providers out there. Ultimately, R3 just needs a single column list of VPN Server IPs that it can randomly choose from should a connection need to be reset. And if you don't have a list? That's fine too... and it will just try to reconnect with whatever server you currently have configured in your VPN Slot. Having created a completely different thread that covers examples how you can pull the necessary VPN Server IP data from various sources, this should give you enough to go on to support your own efforts! I brought a couple of features over from R2, the biggest one being the integration with Unbound. In this day and age of privacy, I believe this is a must-have feature which allows your DNS queries to remain private from your ISP or other monitoring agencies. All in all, R3 is a slimmed down, more efficient and more open version of R2. I hope it serves your purposes well! :)
