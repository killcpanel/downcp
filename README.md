# downcp
The unofficial cPanel uninstall script 

<h3 align="center">downcp</h3>

<p align="center">
  The easy way to nuke cPanel...
  <br>
</p>
# PURPOSE
This script is designed to remove cPanel from a server. cPanel was not designed to be uninstalled and there is really no good reason to ever do this, you're better off re-OSing. This is more of an experiment. If you use this on anything important, you're an idiot.

# HOW IT WORKS
This script does a variety of things, starting by disabling the cPanel service. After doing so, it removes cPanel packages, repos, users, files, crons, services, etc. This script was made with systemd in mind so don't try it on CentOS/RHEL 6.11 or lower servers. Really, you shouldn't try this on anything unless you're a fool, but, oh well.

This script should NOT delete anything non-cPanel. Any databases or site files you have should stay fully intact. Also, this does remove Apache from the server but not MySQL.

# HOW TO RUN IT
```wget https://raw.githubusercontent.com/killcpanel/downcp/master/nuke.sh && chmod +x nuke.sh && sh nuke.sh```

This can take quite some time to run, probably best to start in a screen.

# REQUIREMENTS
- CentOS/RHEL 7+
- Some minimum version of cPanel (TBD, lets say 11.60+)
- Probably EasyApache 4 (TBD, who knows)
- An iron will to remove cPanel, no matter the cost
- Make backups first...