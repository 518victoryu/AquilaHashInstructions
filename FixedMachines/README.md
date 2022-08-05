Authors: Roman Liu, Victor Yu\
Contact: romanliu1220@gmail.com, 518victoryu@protonmail.com
# Fixed Machines
Outputs hashrate data, how many machines were fixed, and how many machines broke in a day.\
Also outputs specific IP addresses that broke or were fixed.
## Example Output
Can also be found in [Example Output File](/FixedMachines/outputfiles/output.xlsx)\
![Output 1](https://i.imgur.com/qt911ul.png)
![Output 2](https://i.imgur.com/AMDW1cM.png)
## Initial Setup
1) Download FixedMachines folder.
2) Make 3 folders with the names:
  - Daily Report A
  - Daily Report L
  - Daily Report Z
3) Download the corresponding daily reports of those customers into those folders. Only works with .csv
  - First file should be a day before the one you want to start on.
    - If you want to start on 6/1/2022 you need to input a 5/31/2022 file
  - Only put daily reports you want to check, the program will check every csv in the folders.
## Running
1) Change .fixedmachines using a text editor of choice for your expected output
  - Syntax:
    - Search All
      - Customer
      - Ex: A
    - Search Lines
      - Customer Line
      - Ex: Zhu J
    - Search between IP Busses
      - Customer LowestIPBus HighestIPBus
      - Ex: Zhu 10.2.17 10.2.30
<img src=https://i.imgur.com/IqHfLDU.jpg alt=".fixedmachines example" height=400 width=auto>
2) Run the FixedMachines.exe file
3) Outputs will be found in the outputfiles directory
