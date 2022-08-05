Authors: Roman Liu, Victor Yu\
Contact: romanliu1220@gmail.com, 518victoryu@protonmail.com
# Debugger.exe
Auto-Debugger for Miners\
Restarts miners between 2 ips and gets their temperatures and summarizes their logs.
## How To Use The Buttons
Select a customer and then hit the X to close the window\
![Button1](https://i.imgur.com/KhNjpeO.png)\
Select an action and then close the window. Search all searches every miner for that customer\
![Button2](https://i.imgur.com/9aU6ffW.png)
### If Lines Chosen:
Select a line and then close the window.\
![ButtonLine](https://i.imgur.com/Ztog1uv.png)
### If Search IPs Chosen:
Type in small IP and then big IP and hit submit then close the window. IPs do not have to exist on the lines.\
EX: \
Small: 10.2.17.0\
Large: 10.2.17.256\
EX2: \
Small: 10.2.0.0\
Large: 10.8.256.256\
![ButtonSearch](https://i.imgur.com/Ts42wDe.png)
# RestartMiners.py
Packages: requests, multiprocessing\
Restarts a miner. Has to be an existing miner.\
Function: restartminers\
Args: \
ip (str) an existing miner\
Return: None\
Usage:\
restartminers('10.2.17.7')
# brokenips.py
Packages: requests, pandas\
Finds the miners that have less than 33% of Factory hashrate.\
Function: getData\
Args: \
customer(str) has to be 'Zhu', 'Lux', or 'A'\
ipsmall(str) can be non existing ip\
iplarge(str) can be non existing ip, must be greater than ipsmall\
Return: a list of IPs of said miners.\
Usage:\
iplist = getData('Zhu','10.2.17.0','10.2.17.256')
# buttons.py
Packages: tkinter\
Button UI to get Customer, ipsmall, and iplarge.\
Function: ipswitcher
Args: None\
Return:\
Customer(str) can be 'Zhu', 'Lux', 'A'\
ipsmall(str) smaller ip address\
iplarge(str) larger ip address\
Usage:\
customer, ipsmall, iplarge = ipswitcher()
# debugger.py
Packages: multiprocessing, pandas\
Python version of debugger.exe\
Refer to debugger.exe for how to run
# logreader.py
Packages: time, re, os, pandas\
Reads Logs and finds common problems in a dir called LOG\
Function: main\
Args: None\
Return: list of [ip, search term, log text]\
Usage: list = main()
# restartanddash.py
Packages: pandas, tkinter, timeit, requests, multiprocessing, os, time, re\
Restarts low hashrate miners between 2 ranges, then gets their temperatures right when they turn on.\
Function: main\
Intended to use with buttons.ipswitcher and brokenips.getData\
Args: iplist (list) list of ips to restart and get temperature data\
Return: listoftemps(list) list of [ip, chain, chip temp, chain, chip temp, chain, chip temp]\
Usage: listoftemps = main(iplist)
# scrapelogs.py
Packages: os, time, timeit, requests, multiprocessing\
Batch downloads logs\
Function: main\
Args: iplist(list) list of IPs to get logs\
Return: None (all logs downloaded are in a dir called LOG)\
Usage: main(iplist)

