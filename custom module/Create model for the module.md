<h1> Step 1 </h1> 
We are continuing from this step : https://github.com/shyammaurya1/Odoo/blob/main/custom%20module/create%20custom%20module.md
(Go through it if you have not gone through it yet!)

<h1> Step 2 </h1>
Create a file in test directory as "__init__.py">
write in this file as  : 

```
from . import person
```

<h1> Step 3 </h1>
Create a file as "person.py"
write in this file as : 

```
from odoo import models

class Hperson(models.Model):
      _name = 'h.person'
      _description = 'h.record'
```

<h1> Step 4 </h1>
Restart the server!

<h1> Step 5 </h1>
Click on update app list
Search for your module in search section

<h1> Step 6 </h1>
Install the module.

(Check if the model is created or not)
<h1> Step 7 </h1>
Go to settings
click on technical, you will find "models" option under database structure

<h1> Step 8 </h1>
search for person
(you will find model for person got created)

(For defining fields)
<h1> Step 9 </h1>

```
from odoo import models, fields

class Hperson(models.Model):
      _name = 'h.person'
      _description = 'h.record'
      
      person_name = fields.Char(string = 'Name', required = True)
      person_age = fields.Integer('Age')
      notes = fields.Text(string = 'Notes')
      image = fields.binary(string = 'Image')
      
```

<h1> step 10 </h1>
Restart the server
<br></br>
Update the module




  
