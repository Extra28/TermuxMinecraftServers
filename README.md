# TermuxMinecraftServers
A documentation of how I made a bunch of android phones run termux concurrently to create a minecraft server cluster

* phone 1 ip: 192.168.50.215
* phone 2 ip: 192.168.50.184
* phone 3 ip: 192.168.50.126
* command to ssh cuz termux openssh uses port 8022 for some reason:
sudo ssh -i ./id_rsa -p 8022 (insert IP here)

to do list plan!:
* set up prometheus on all phones, along with a script to run termux-battery-status and have it set up on a http localhost so that it can be read by prometheus.
* grafana to record all these metrics
* python script using kasa to make it so that if battery is above 80 percent, turn off charger and if below 25 then turn on charger. must get tplink power strip first.
* set up mc server on one phone to ensure it works
* then figure out how to link the 3 phones tgt so they run in a cluster and that if one phone goes down the server will still run without interruptions. also if phone goes down then send me an email notification?
