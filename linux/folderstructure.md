root@Ubuntu-dev:/# -> this is the path when we are logged in using docker environment.<br>

here root is a user.<br>
     Ubuntu-dev is a hostname.<br>
     :,# is a separators
     / is this means you are at the root of your file system.<br>

Ubuntu@hostname:~$

here Ubuntu is a user<br>
     ~ is a Tilt<br>

Apart form the root user it created anothere user called ubuntu. it is a security purpose EC2 instance didn't want to grant you root user or administrative permission out of box that's why default sign is Ubuntu user. so it will have less permissions when compared to root.<br>
Tilt is a home directory of any user that you logged in.<br>
Ex: default is /home/Ubuntu.<br>

◇ Linux Environment has the package of 'ls' already installed that's why when we entered the 'ls' command then it will list all of the files and folders which are present.<br>

'ls': list -> it will list all of the folders and files in the particular directory.<br>

'mkdir': it creates a new folder.

'sudo su -': it will switch to the root user.

'cd /': it will take you to the root location of the file system.

'sbin': sbin means system binaries that means commands or binary files that you can use to manage your system as an administrator.

'ls /sbin/': if we give like this then it will list a lot of system binaries in this particular folder i.e. sbin <br>
Ex: useradd: this is to add the user<br> 
    groupadd: to add the group<br>
    userdel: to delete the user<br>
    groupdel: to delete the group.<br>
all these are present in system binaries.

'lib': it means libraries.<br>
'ls /lib/': these are used by linux kernel for making system calls with the hardware (or) to execute its action.<br>

'boot': this will help the linux machine to restart or start the linux machine.whatever inside the folder, it will help to the linux machine like commands is required while restart or start the linux or action that it needs to execute during the start of the machine.<br>

'bin': this is for user binaries.<br>
'ls /bin/': we can see list of the commands which is present in this folder.<br>

◇Anyone can access this bin folder (or) whatever commands present in this bin folder.<br>
Ex: date, diff, linnk, mount or sed.<br>
◇ All of the commands/binaries inside bin folder are non-administrative.<br>

◇ Linux admin can give access of the sbin folder to system administrative and bin folder access to the users (or) everyone.

◇ This sbin and bin folders which is present under '/usr' folder.<br>

'usr': This folder many directories (or) folders but most important folders sbin, lib and bin.<br>

'srv': it means server where you can store any configuration files (or) any important info related to webservers. By Default, when we create some webservers, it will actually store some files in this srv.<br>

'opt': it is a very important folder. this is a common location for all third party dependencies.<br>

'mnt': This is used by the linux administrators to mount the new volumes.<br>

'var': Majorly, it is used for log files storing or maybe third party libraries or libraries that you've download from the internet. Apache or http ..etc.. like this kind of logs are stored in /var/log folder.

'home': Anyone can acess this folder and anyone can create a folders under this home directory using two commands to create a user.<br>
1)adduser
2)useradd

Note: useradd command creates user but doesn't create a home directory.<br>

'data': it is used for storing the data.<br>

◇ Organizational billinng info (or) organizational cloud cost (or) organization any data that can be shared with other people in the organization (or) other admin in the organization. you can put that within data. it depends on how you restrict the access to the folder. this is not permanent data.<br>

'proc': it is virtual file  system for your process and system info.<br>

◇ Proc and dev folders are temporary folders where you can store files that are not permanent.<br>

'tmp': it is a temporary folder. Generally, when you're writing scripts and script generates a log file. suppose if we want to delete that after a while then we can put that in this tmp folder.<br>
 Ex: This tmp folder is like deleted photos (or) videos that will permanently deletes after 30days and until it stores those in temporary folder. in sameway, this tmp folder also stores the deleted any files or log files that we want to delete after a while.<br>

'root': root is a root directory or home directory. /root is only exception, only for root the home directory is /root. rest any user that you create home directory is start with /home i.e. they are insde the /home folder this is the only exception.<br>

'run': run is basically stores the runtime data of the process.<br>

◇ while process is running then if it has runtime data i.e. stored within the 'run' folder.
'etc': we can have all system configuration files. using these files, we can configure or modify the system.<br>
Ex: This is like setting in our phone or laptop.
         (or)
Ex-1: passwd is a password, using this you can modify password of any user on the linux machine.<br>
Ex-2: host: it is a file where you can add local DNS caching for your linux environment, maybe we can say that this particular website has this IP address.<br>
Ex-3: OS-release: this is for OS details. if we do cat /etc/OS-release then we can see all the details of linux environment.<br>

Q)How Linux Kernel is able to execute of 'ls' command? what is the actual location of 'ls'?<br>
A)There is a something called as PATH on your linux machine. this is also available on windows as well. we might not use regularly. this will tell the linux that when someone enters the command or when someone writes something on the terminal. Basically check in all the folders within the path. it is one of that folders you can directly execute it.<br>
echo $PATH<br>
then you will get /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin<br>
if 'ls' command is in one of the folder then it will execute it and it is in /usr/bin and /usr/bin is in the PATH. that's why it is executed.<br>
which 'ls' then you will get /usr/bin/ls.<br>
