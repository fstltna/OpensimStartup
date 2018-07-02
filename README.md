# Opensim Startup Scripts (1.0.0)
Startup scripts for the Opensim virtual world software - uses the "screen" command to manage session. This also restarts the Opensim process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/OpensimStartup) - [Official Forum](https://opensimcity.org/index.php/forum/server-software)

---
These start up the Lugdunon server at boot time with a "screen" process.

1. Copy **opensim** into **/etc/init.d** - make sure it is executable
2. Copy **startopensim** into **/root/opensim** - make sure it is executable
3. Run "**systemctl enable opensim**" (only needed once, will stick)
4. Run "**systemctl start opensim**" - starts Opensim without restarting the server

When you want to view the Opensim console, just enter "**screen -r**" in your shell.

To disconnect from the Opensim console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /root/opensim/nostart**". To reenable it type "**rm /root/opensim/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
