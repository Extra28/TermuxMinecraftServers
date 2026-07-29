# TermuxMinecraftServers
A documentation of how I made a bunch of android phones run termux concurrently to create a minecraft server cluster

phone 1 ip: 192.168.50.215
phone 2 ip: 192.168.50.184
command to ssh cuz termux openssh uses port 8022 for some reason:
sudo ssh -i ./id_rsa -p 8022 (insert IP here)

next to do:
prometheus and grafana stuff
implement android battery scraping also cuz need to monitor battery life
if can consistently monitor battery then buy smart power strip frm tp link and figure out how to run script for said smart power strip
