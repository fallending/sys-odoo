# group

<group>标签允许组织Form表单里的内容。


??? 相当于。section？？？

## 用法

```
<sheet>
   <group name="group_top">
       <group name="group_left">
           <field name="name"/>
       </group>
       <group name="group_right">
           <field name="is_done"/>
           <field name="active" readonly="1"/>
       </group>
   </group>
</sheet>
```

## 解释


在<group>中放置<group>，可以创建一个两列的列表。Group标签使用时，建议定义它的name属性，这样可以更方便的让其它模块扩展它。

使用<group>标签，可以更好的规划需要展示内容。


## 技巧