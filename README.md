# Opensim Startup Scripts (1.1.1)
Startup scripts for the Opensim virtual world software - uses the "screen" command to manage session. This also restarts the Opensim process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/OpensimStartup) - [Official Forum](https://opensimcity.gameplayer.club/index.php/opensimforum/our-opensim-tools)

---
These start up the Opensim server at boot time with a "screen" process.

1. Copy **opensim** into **/home/osowner/bin** - make sure it is executable
2. Copy **startopensim** into **/home/osowner/opensim** - make sure it is executable
3. Add this to the crontab:

    @reboot /home/osowner/bin/opensim start


When you want to view the Opensim console, just enter "**screen -r**" in your shell.

To disconnect from the Opensim console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 20.04 server...

If you want to turn off the server respawning type "**touch /home/osowner/opensim/nostart**". To reenable it type "**rm /home/osowner/opensim/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
