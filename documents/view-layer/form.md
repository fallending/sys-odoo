# 完整的form视图


## 用法

```
<form>
       <header>
           <button name="do_toggle_done" type="object" string="Toggle Done" class="oe_highlight" />
           <button name="do_clear_done" type="object" string="Clear All Done" />
       </header>
       <sheet>
           <group name="group_top">
               <group name="group_left">
                   <field name="name"/>
               </group>
               <group name="group_right">
                   <field name="is_done"/>
                   <field name="active" readonly="1" />
               </group>
           </group>
       </sheet>
   </form>
```