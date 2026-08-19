# TermuxMinecraftServers
A documentation of how I made a bunch of android phones run termux concurrently to create a minecraft server cluster

notes:

* phone 1 ip: 192.168.50.215
* phone 2 ip: 192.168.50.184
* phone 3 ip: 192.168.50.126
* command to ssh cuz termux openssh uses port 8022 for some reason:
sudo ssh -i ./id_rsa -p 8022 (insert IP here)

* prometheus port is 9090
* node exporter port is 9100
* for node exporter, as long as collecting timex and selinux are disabled (--no-collector.timex and --no-collector.selinux respectively), node exporter will not crash. stats returned might be incomplete, but better than nothing

to do list plan!:
* set up prometheus on all phones, along with a script to run termux-battery-status and have it set up on a http localhost so that it can be read by prometheus. done!
* grafana to record all these metrics. done!
* so almost everything about the python kasa library is vibecoded and sometimes their own examples dont work as intended, i might just end up writing somethig myself if i cant figure something out.
* set up mc server on one phone to ensure it works 
* link 3 phones tgt using velocity and maybe multipaper, to allow for horizontal scaling, however no mods. alternatively, use regular paper but that means no horizontal scaling, aka defeating the whole purpose of this project. i guess i could learn java or something???? make a multipaper thing but for fabric????? to allow for mods??? feels like more work than whats worth but sigh ok maybe i shld.
