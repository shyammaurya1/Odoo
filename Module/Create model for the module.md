<h1> Step 1 </h1> 
We are continuing from this step : https://github.com/shyammaurya1/Odoo/blob/main/custom%20module/create%20custom%20module.md
(Go through it if you have not gone through it yet!)

<h1> Step 2 </h1>
crete a file as "__init__.py" in test directory
write in this file as : 

```
from . import models
```

<h1> Step 3 </h1>
Create a directory as 'models' in 'test' directory 
create a file in models directory as '__init__.py'
write in this file as  : 

```
from . import person
```

<h1> Step 4 </h1>
Create a file as "person.py" in models directory
write in this file as : 

```
# -*- coding: utf-8 -*-
from odoo import api, fields, models

class HospitalPatient(models.Model):
    _name = "hospital.patient"
    _description = "Hospital Patient"

    name = fields.Char(string='Account Type', required=True, translate=True)
    age = fields.Integer(string='Age')
    gender = fields.Selection([
        ('male', 'Male'),
        ('female', 'Female'),
        ('other', 'other'),
    ], required=True, default='male')
    note = fields.Text(string='Description')

```

<h1> Step 5 </h1>
Restart the server!

<h1> Step 6 </h1>
Click on update app list
Upgrade the module 
Install it if not installed yet.


(Check if the model is created or not)
<h1> Step  </h1>
Go to settings
click on technical, you will find "models" option under database structure

<h1> Step 8 </h1>
search for hospital
(you will find model for hospital got created)






  
