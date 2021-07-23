<h1> Step 1 </h1> 
We are continuing from this step : https://github.com/shyammaurya1/Odoo/blob/main/custom%20module/create%20custom%20module.md
(Go thorugh it if you have not gone through it)

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
from odoo import modules

class Hperson(models.Model):
      _name = 'h.person'
      _description = 'h.record'
```

<h1> Step 4 </h1>



  
