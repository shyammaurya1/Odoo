# Odoo

The Following instructions are compatible with Ubuntu 20.04(recommended) for Odoo 14 Community Version Installation
Using Python 3.8.2



<H>Step 1 : Update Server</H>
-------------------------

sudo add-apt-repository universe

sudo apt-get update

sudo apt-get upgrade -y


Step - 2: PPA
---------------------------------

sudo add-apt-repository ppa:deadsnakes/ppa


Step - 3: Installing Python package for the Environement
----------------------------------------------------------

for python 3.8-
sudo apt-get install python3.8 python3.8-dev python3.8-venv


Step 4:Python Dependencies
------------------------------------------------
sudo apt-get install virtualenv

virtualenv python3-psycopg2 libpq-dev libxml2-dev libxslt-dev libxslt1-dev zlib1g-dev python3-pip libjpeg8-dev python3-ldap libldap2-dev libsasl2-dev nodejs npm node-less unzip git

-----python3-ldap problem fix ------

sudo apt-get install python-ldap
sudo apt-get install python-dev
sudo apt-get install libldap2-dev
sudo apt-get install libsasl2-dev
sudo apt-get install python-ldap
pip3 install python-ldap



Step -5: Set Up Symlinks

(references about symbolic links - https://unix.stackexchange.com/questions/26896/how-does-linux-work-with-symbolic-links)
-------------------------------------------------------------------------------------------------------------------------
sudo ln -s /usr/lib/x86_64-linux-gnu/libjpeg.so /usr/lib
sudo ln -s /usr/bin/nodejs /usr/bin/node



Step - 6: Set up postgresql (Required for Database Managment)
------------------------------

sudo apt-get install postgresql -y


**create a database user**

sudo su postgres


**username**

createuser --createdb --username postgres --no-createrole --no-superuser --pwprompt <user_name>

(Use exit command to stop the postgresql works)




Step - 7 : Install wkhtmltopdf if you haven’t installed it yet in your local PC.
----------------------------------------------------------------------------------
***
Wkhtmltopdf is an open source simple and much effective command-line shell utility that enables user to convert any given HTML (Web Page) to PDF document or an image (jpg, png, etc)
***


sudo add-apt-repository ppa:ecometrica/servers

sudo apt-get update

sudo apt-get install wkhtmltopdf 

**create user for wkhtmltopdf**
useradd -m -g sudo -s /bin/bash odoo14
passwd odoo14
su odoo14





Step - 8: Clone Odoo 14 files from Odoo
-----------------------------------------------------------
git clone https://github.com/odoo/odoo.git --depth 1 --branch 13.0 --single-branch odoo13

>> Virtual Environemnt

virtualenv -p python3.8 env
source env/bin/activate

-----*Use the requirments.txt file given with my files and replace it with odoo13/requirments file.*------

pip install -r odoo13/requirements.txt   ---If any pip error given,install them manually using pip3 install <packagename>
pip install -r odoo13/doc/requirements.txt


-------------python -pydlab install -------------------

sudo apt-get install python-ldap
sudo apt-get install python-dev
sudo apt-get install libldap2-dev
sudo apt-get install libsasl2-dev
sudo apt-get install python-ldap
pip3 install python-ldap



Done with the installation Phase,Now for the Setup-

In the venv ,go to the odoo14 folder and run - python odoo-bin

Go to http://localhost:8069/ 

And boom Odoo Running!










