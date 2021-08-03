
<h1> Step 1 </h1>
create a directory in "test" directory as "views"

<h2> Step 2 </h2>
create a file as "patient.xml",
write into as : 

```
<?xml version="1.0" encoding="UTF-8"?>
<odoo>
```
(This is for adding action)
```
    <record id="patient_action" model="ir.actions.act_window">
        <field name="name">Patients</field>
        <field name="type">ir.actions.act_window</field>
        <field name="res_model">hospital.patient</field>
        <field name="view_mode">tree,kanban,form</field>
        <field name="help" type="html">
            <p class="o_view_nocontent_smiling_face">
                 create your first patient!
            </p>     
        </field>
    </record>  
```
(This is for creating menu)
```


<menuitem id="hospital_root"
          name = "Hospital"
          sequence="10" />

<menuitem id="hospital_patient_root"
          name="Patients"
          parent="hospital_root"
          sequence="10" />

<menuitem id="hospital_patient_"
          name="Patients"
          parent="hospital_patient_root"
          action="patient_action"
          sequence="10" />                    
</odoo>
```
(This is to check installation)
<h1> Step 3 </h1>
Restart the server
<br></br>
Upgrade the module
<br></br>
Go onto settings
<br></br>
Under user interface, click on "Menu Items"
<br></br>
search in search section as"hospital"






