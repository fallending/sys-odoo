# 搜索


## 用法

```
<record id="view_filter_todo_task" model="ir.ui.view"> 
 <field name="name">To-do Task Filter</field> 
 <field name="model">todo.task</field> 
 <field name="arch" type="xml"> 
   <search> 
     <field name="name"/> 
     <filter string="Not Done" 
       domain="[('is_done','=',False)]"/> 
     <filter string="Done" 
       domain="[('is_done','!=',False)]"/> 
   </search> 
 </field> 
</record> 
```

## 解释

列表的右上角，Odoo显示一个搜索框。 它搜索的字段和可用的过滤器是由<search>视图定义的。

<field>元素定义了在搜索框中输入时也能搜索的字段。 <filter>元素添加了预定义的过滤条件(过滤条件可以通过用户点击来切换），是使用特定语法来定义的