
------------------------
## 最需要
------------------------

* [odoo model 的常用方法](https://blog.csdn.net/catstarxcode/article/details/80367620)
* [官方文档](https://www.odoo.com/documentation/12.0/)
* [dashboard参考1](https://www.odoo.com/apps/modules/11.0/hrms_dashboard), [dashboard参考2](https://www.odoo.com/apps/modules/11.0/hr_dashboard)
* 常规开发参考：https://www.kancloud.cn/hx78/odoo_10/416235
* [ICon搜索](http://www.iconfont.cn/home/index?spm=a313x.7781069.1998910419.2)

------------------------
## QWeb 指令
## http://www.odoov.com/index.php?title=%E4%BD%BF%E7%94%A8t-att%E4%BD%9C%E4%B8%BA%E5%8A%A8%E6%80%81%E5%B1%9E%E6%80%A7
------------------------

```
// t-foreach
<t t-foreach="record.message_partner_ids.raw_value" t-as="rec">
	<t t-esc="rec" />
</t>

//
t-att-src="kanban_image('res.users', 'image_small', record.user_id.raw_value)"

// t-if
<t t-if="record.effort_estimate.raw_value gt 0">
	<li>
		Estimate <field name="effort_estimate"/>
	</li>
</t>
```

------------------------
## 代码规范
------------------------

```
_glolal_val_ = None

class Sample(object):
 _ = ''
 _property = ''
 _result_repo

 def test(self): # public 方法
 	val = 0

 	return val

 def _test(self): # private 方法
 	pass
```

------------------------
## 第一阶段：常规开发
------------------------

* [odoo10 学习笔记2（简单的请假模块）](https://www.jianshu.com/p/7b154004cfe1)，[他的其他博客](https://www.jianshu.com/u/d4607d4b7c50)
* [odoo10 学习笔记3(权限管理)](https://www.jianshu.com/p/bc4e9db349a2)

## /??

* [需要看](https://blog.csdn.net/j_z10/article/category/6272798)

## 菜单

* [Odoo开发手册-菜单项操作](https://blog.csdn.net/tom21s/article/details/51737748)

## 视图

* [odoo10普通视图添加自定义css和自定义js](https://blog.csdn.net/qingtianjushi/article/details/78597040?utm_source=blogxgwz7)

* [odoo10参考系列--视图二（表单视图）](https://blog.csdn.net/mzl87/article/details/79752670?utm_source=blogxgwz23)

## Widget

* [odoo常用的widget](https://blog.csdn.net/Beyond_F4/article/details/82458801?utm_source=blogxgwz4)

* [odoo 自定义 widgets (二)](https://blog.csdn.net/weixin_37583798/article/details/81201458?utm_source=blogxgwz1)

* 用法？？？？？

## Action

* [odoo10参考系列--操作（Actions）](https://blog.csdn.net/mzl87/article/details/79754834?utm_source=blogxgwz18)


## 模型

* [doo中使用的数据模型](https://www.cnblogs.com/hellojesson/p/7061010.html)
* [Odoo字段类型](http://www.cnblogs.com/cnodoo/p/9278620.html)

```
基础类型：char, text, boolean, integer, float, date, time, datetime, binary 
关系类型：one2one, one2many, many2one, many2many 
复杂类型：selection, function, related
```

* [odoo 如何给所有的model添加一个通用的方法 （类似 create，write）](https://blog.csdn.net/cl123cpzaihu/article/details/81326281)

* [Odoo10开发教程三（模型关联）](https://www.jianshu.com/p/555a18060514)

* [odoo V10中文参考手册（一：ORM API）](https://www.jianshu.com/p/88f6f79756be)

* [odoorpc](https://pythonhosted.org/OdooRPC/tuto_browse.html)

* [API 装饰器 @api.one @api.multi @api.model区别](https://stackoverflow.com/questions/31112660/what-is-different-b-w-api-one-api-multi-and-api-model)，其他百度的国内文章可以不必看了，很多在瞎说

## Web

* [Odoo Web前端界面详解 - 1](https://blog.csdn.net/J_z10/article/details/79247533?utm_source=blogxgwz0)

* [odoo10参考系列--网络控制器（Web Controllers）](https://blog.csdn.net/mzl87/article/details/79787756)

## module

* [odoo10 学习笔记2（简单的请假模块）](https://www.jianshu.com/p/7b154004cfe1)



------------------------
## 第二阶段：升级
------------------------

## 工作流

* [workflows](https://www.odoo.com/documentation/10.0/reference/workflows.html)

## UI升级：ir.actions.client

* [odoo10参考系列--操作（Actions）](https://blog.csdn.net/mzl87/article/details/79754834)
* [Odoo 创建特定布局的页面](https://blog.csdn.net/Pompeii/article/details/76098344?utm_source=blogxgwz0)

## [QWeb](https://www.odoo.com/documentation/12.0/reference/qweb.html)


------------------------
## 第3阶段：Bootstrap
## https://v3.bootcss.com/css/
------------------------

## 对其方式

```
<p class="text-left">Left aligned text.</p>
<p class="text-center">Center aligned text.</p>
<p class="text-right">Right aligned text.</p>

// button 按钮靠右布局
父div 增加样式 text-align:right;

// 左右对齐
div可以使用pull-right, text-center, pull-left
```


## 栅栏方式

```
row
```


## display 属性

*规定元素应该生成的框的类型*