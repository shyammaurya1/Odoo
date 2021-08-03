By giving access rights, module will be displayed in the menu section.


<H1> Step 1 </H1>
Enable superuser mode
Click on Debug icon(Developer tools)
Click on "Become Superuser"

<h1> Step2 </H1>
(Backend)
<br></br>
Open module folder (custom)
<br></br>
Create a directory as "security"

<h1>Step 3</h1>
Create a file as as "ir.model.csv"
<br></br>
write into this as : 

```
id,name,model_id:id,group_id:id,perm_read,perm_write,perm_create,perm_unlink
access_hospital_patient,access.hospital.patient,model_hospital_patient,,1,1,1,1
```
<h1>Step 4</h1>
Add this file path in "__manifest__.py" as

```
'data' : 'security/ir.model.access.csv','person.xml',
```
<h1> Step 5 </h1>
Restart the server

<h1> Step 6</h1>
(Frontend)
<br></br>
Update/Upgrade the module

<h1> Step 7</h1>
go to settings->technical, click on access rights under security

<h1> Step 8</h1>
Check the access right by searching by module name in search section.
here, search as "access.hospital.patient"

<h1> Step 9</h1>
check in menu, you can see your module name as submenu
<br></br>
If you want to remove it from menu, archive it!







