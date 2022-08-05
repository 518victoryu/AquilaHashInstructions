Authors: Roman Liu, Victor Yu\
Contact: romanliu1220@gmail.com, 518victoryu@protonmail.com
# dailyhash.py
logs daily changes in hashrate and other important stats
Packages: enum, pandas, datetime, time, requests, dataclasses, json, os\
Usage: run dailyhash.py in the terminal.\
Make sure the excel sheet is placed in a dir called TestFiles with the files named:\
'Z-Daily-Hashrate.xlsx', 'L-Daily-Hashrate.xlsx', 'A-Daily-Hashrate.xlsx'\
In a text file called subaccount.txt, write down subaccounts to log to the excel sheet.\
In the corresponding excel sheet add in the rows for subaccounts.
