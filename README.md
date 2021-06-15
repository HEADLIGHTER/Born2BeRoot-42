
# Born2BeRoot 42/21

# !!monitoring.sh script WIP!!
What's working? Almost everyting except LVM check. I'll fix it ASAP.

# Please, DO NOT copie + paste this thing with emptiness in your eyes and blank in your head!
It's highly recommended to know what u use and how&why it works. At least, it will be usefull for YOURS and ONLY YOURS defense.
Google/man all the commands listed here and read about it's options/parameters/etc. Be intellegent, be adaptive, be SMART. Know the tool you use.
Still, it's Work In Progress version of script, so use it in your project on your own risk. A lot of things may change and should be changed!
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
To make this works u need to [$ chmod +x monitoring.sh] (ofc lol) and [$ sudo chown root monitoring.sh], [$ sudo chmod u+s monitoring.sh] to run 
this script as root (and remove these "sudo" commands from script to prevent counitng them in our "The number of commands executed with the sudo 
programm"). Please note that after these operations u can edit script file only from root.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
# How to use
First off [$ sudo crontab -e]. Set nano/vi as your text redactor for cron and add next lines in your crontab file:
~~~~~~~~~~~~~~~~~~~~~~~~~~
@reboot /path/to/file/monitoring.sh
10 * * * * /path/to/file/monitoring.sh
~~~~~~~~~~~~~~~~~~~~~~~~~~
Dont forget that you should write FULL PATH TO FILE (no ~/*/etc.) due to cron's pecularity.
