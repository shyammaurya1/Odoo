<h1> Step 1 </h1>
Go in the module's folder in which you want to add fields
there is a python module file, let us take it as "person.py"

<h1> Step 2 </h1>
Open "person.py"
add this :

```
class SalesOrderInherit(models.Model):
     _inherit = 'sale.order'
     
     patient_name = fields.char(string = 'Patient Name')
```

<h1> Step 3 </h1>
Open views folder, there you will find related xml file
<br></br>
let us take it as person.xml 

<h1> Step 4 </h1>
write this over there : 

```
<record id="sale_order_inherit" model="ir.ui.view">
  <field name="name">sale.order.inherit</field>
  <field name="model">sale.order</field>
  <field name="inherit_id" ref="sale.view_order_form"/>
 <field name="arch" type="xml">
  <field name="partner_id" position="after">
    <field name="patient_name"/>
  </field>
 </field>
</record>
```

<h1> Step 5 </h1>
Restart the server
<br></br>
update the app list

<h1> Step 6 </h1>
Upgrade the module
(Check if field is added or not)











