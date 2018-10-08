# odoo 模块

## Odoo常用功能模块

企业管理模块

物料管理模块

财务管理模块

人力资源模块

客户与供应商关系管理模块

项目管理模块

日常工作管理模块

沟通工具模块

业务流程管理模块

## 模块开发流程

1：分析模块模型，得出模型所需的字段有哪些，然后定义模型类——python编程。

2：构建菜单对象——在views文件夹下，使用xml定义菜单项。

3：构建动作对象，关联某个具体菜单项的响应。

4：构建视图对象：主要是list、tree、form、search视图。

5：配置__init__.py和__manifest__.py

*Odoo依赖这两个文件去识别一个文件夹下是否保存一个模块*

```
{
    'name':"模块名称",
    'summary':"模块概述",
    'version':'版本',
    'category':'模块所属分类',
    'sequence':模块在应用菜单中的序号位置,
    'author':'开发者名字',
    'website':'网站',
    'depends':['依赖模块（需要用到其他模块的内容，则填写依赖模块的名字）在安装本模块时，会先安装依赖模块'],
    'data':['数据文件.xml'],
    'qweb':['视图文件.xml'],
    'demo':['默认添加的示范数据.xml'],
    'test':['测试数据.xml'],
    'installable':True,                    // 默认True，可设为False禁用该模块
    'application':True,                    // 默认False，如果设为True，则这个模块成为一个应用了。你的主要模块建议设置为True，这样进入Odoo后点击本地模块，然后默认的搜索过滤就是 应用 ，这样你的主模块会显示出来。
    'auto_install':False,                  // 默认False，如果设为True，则根据其依赖模块，如果依赖模块都安装了，那么这个模块将自动安装，这种模块通常作为胶合(glue)模块。
    'description':'''模块详细描述''',
}
```

6. 为模块添加图片

新建static目录，创建descrpition文件夹。 在其中，放入一个名为"icon"的图片文件，切记：odoo依靠文件名来识别，所以必须是icon命名。 之后，就可以在应用列表看到自己的模块了。

7. __init__.py的使用

该文件用于导入模块中需要用到的python类文件。

为了方便管理，我们一般这样做：新建一个models文件夹，在其中存放python的实体类。models目录下新建一个__init__.py，在其中import 该目录下所有实体类。 然后在模块的__init__.py中，Import models 即可。

## [odoo10学习笔记二：继承（扩展）、模块数据](https://www.cnblogs.com/qjtjh/p/8269617.html)

Odoo开发的一条黄金准则是——不要修改现有的模块，以免改动后的代码与原有模块产生混淆。

odoo提供了继承机制，我们可以选择一个基础模块，然后继承它，在它的基础上进行修改、扩展，生成自己的模块。

开发自己的模块时，需要在模块所在目录下，创建两个文件：__init__.py和__manifest__.py，在其中定义模块的初始化操作以及模块的描述。

### 模块文件目录构成：

data：存放demo和data xml

models：存放模型定义：继承models.Model类，定义出的模型类会自动与Odoo提供的ORM接口匹配，也就是说这些模型类会自动存入sql中。

controllers：存放http路径控制（url请求处理）

views：网页视图文件与模版文件（xml文件，使用QWEB语言进行描述）

static：静态资源文件，如css、js等

security：对模块的访问权限控制，在ir.model.access.csv文件中定义。还可以新建一个record_rule.xml，在其中进行更细化的权限控制。

继承模块通过 _inherit=“继承的模块”  属性来实现。之后在新创建的模块中就可以新增field、修改父模块的field、重载方法了。

 
视图文件也可继承修改，对与视图文件中某个标签，通过 ref=“继承的视图元素”进行继承。

## 数据端开发

可以使用pgadmin3来对postgreSQL数据库管理操作，如果SQLYog操作mysql一样。

