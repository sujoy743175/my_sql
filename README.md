sudo apt-get update
sudo apt-get upgrade
sudo apt install build-essential dkms linux-headers-$(uname -r)

insert guest addition cd now


restart the machine

---- install google chrome 

wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb

sudo apt install ./google-chrome-stable_current_amd64.deb

---- install terminator------------

sudo apt-get update

sudo apt install terminator

--------install pip3-------------
sudo apt install python3-pip


------install latest python--------------

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
sudo su

cd

cd /usr/src/          -----(next time use cd/usr/bin)

wget https://www.python.org/ftp/python/3.9.6/Python-3.9.6.tgz


tar -xf Python-3.9.6.tar.xz

cd Python--3.9.6

./configure --enable-optimizations --with-ensurepip=install

make -j8

make altinstall

update-alternatives --install /usr/bin/python python /usr/bin/python3.8 2
update-alternatives --install /usr/bin/python python /usr/bin/python3.9 3


update-alternatives --config python


-----and choose the python version and press enter---------------

............vs code installation .............

sudo snap install --classic code


-------------install git------------

sudo apt install git

-----------
<<<<<<<<<mysqlworkbench>>>>>>>>>>>>>>>>>
Download APT repository from official

sudo dpkg -i mysql-apt-config_0.8.18-1_all.deb

sudo apt update
sudo apt upgrade

sudo apt install mysql-workbench-community
mysql-workbench

.......voilaaaaa   !.......






<<<<<<root password change>>>>>>
systemctl status mysql.service    ---- check status

robotics@robotics-VirtualBox:~$ mysql -uroot -p
Enter password: 
ERROR 1698 (28000): Access denied for user 'root'@'localhost'

sudo mysql

mysql> use mysql;

select user, authentication_string, plugin, host from mysql.user;

show variables like 'validate_passwords%';

mysql> quit
Bye

sudo mysql_secure_installation

--------------ente all y----------------

then exit and close the terminal

reopen terminal

robotics@robotics-VirtualBox:~$ mysql -u root -p
Enter password: 
ERROR 1698 (28000): Access denied for user 'root'@'localhost'


sudo mysql

show databases;

use mysql;

select user, authentication_string, plugin, host from mysql.user;

show variables like 'validate_passwords%';

mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH caching_sha2_password BY 'Sujoy$743175';

Query OK, 0 rows affected (0.17 sec)

then exit and close the terminal

reopen terminal

robotics@robotics-VirtualBox:~$ mysql -u root -p

-----enter password newly created-----------

select user, authentication_string, plugin, host from mysql.user;


...........annnddd Voilaaa !.... see the password has changed

----------install python-connector------------

pip3 install mysql-connector-python






