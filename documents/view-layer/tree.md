# 列表


## 用法


```
<record id="view_tree_todo_task" model="ir.ui.view"> 
 <field name="name">To-do Task Tree</field> 
 <field name="model">todo.task</field> 
 <field name="arch" type="xml"> 
   <tree decoration-muted="is_done==True"> 
     <field name="name"/> 
     <field name="is_done"/> 
   </tree> 
 </field> 
</record>
```