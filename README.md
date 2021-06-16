
# Born2BeRoot 42/21

Developed for Debian so i'm not sure that it will run properly on CentOS distributive. Anyway, PM me on Discord if its working on CentOS or you have a suggestion/issues: MMBHWR#0793

# monitoring.sh script wip
Known issues: 
1) For some reason script display system information twice when you execute it with [$ ./monitoring.sh] but everything works pretty well while running by cron. I'll try to find a solution for this.
2) Cron may refuse to running script on boot due to bug in Debian (https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=635473). How to fix? [https://bugs.debian.org/cgi-bin/bugreport.cgi?att=0;bug=635473;msg=70]. Good luck :) Maybe someday i'll make script that would be able to fix this issue in one command.

# Please, DO NOT copie + paste this thing with emptiness in your eyes and blank in your head!
It's highly recommended to know what u use and how&why it works even if i leaved an explanation in commentary. At least, it will be usefull for YOURS and ONLY YOURS defense. Google&man all the commands listed here and read about it's options/parameters/etc. Be intellegent, be adaptive, be SMART. Know the tool you use.
Still, it's Work In Progress version of script, so use it in your project on your own risk because i haven't validated it yet. A lot of things may change and should be changed!
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
To make this works u need to [$ chmod +x monitoring.sh] (ofc lol) 
and [$ sudo chown rootmonitoring.sh], [$ sudo chmod u+s monitoring.sh] to run 
this script as root (and remove these "sudo" commands from script to prevent 
counitng them in our "The number of commands executed with the sudo 
programm"). Please note that after these operations u can edit 
script file only from root (and it won't show the number of executed sudo commands
if you running script as user).
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
# How to use
First off [$ sudo crontab -e] (yep, you need sudo to make cron runnig script as root.[$ crontab-e] will open another file that will run your script as user). Set nano/vi as your text editor for cron and add next lines in your crontab file:
~~~~~~~~~~~~~~~~~~~~~~~~~~
@reboot /path/to/file/monitoring.sh
*/10 * * * * /path/to/file/monitoring.sh
~~~~~~~~~~~~~~~~~~~~~~~~~~
Dont forget that you should write FULL PATH TO FILE (no ~/*/etc.) due to cron's pecularity.
