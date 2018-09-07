Odoo
----

A suite of web based open source business apps:

<a href="https://www.odoo.com/page/crm">Open Source CRM</a>,
<a href="https://www.odoo.com/page/website-builder">Website Builder</a>,
<a href="https://www.odoo.com/page/e-commerce">eCommerce</a>,
<a href="https://www.odoo.com/page/warehouse">Warehouse Management</a>,
<a href="https://www.odoo.com/page/project-management">Project Management</a>,
<a href="https://www.odoo.com/page/accounting">Billing &amp; Accounting</a>,
<a href="https://www.odoo.com/page/point-of-sale">Point of Sale</a>,
<a href="https://www.odoo.com/page/employees">Human Resources</a>,
<a href="https://www.odoo.com/page/lead-automation">Marketing</a>,
<a href="https://www.odoo.com/page/manufacturing">Manufacturing</a>,
<a href="https://www.odoo.com/page/purchase">Purchase Management</a>,
<a href="https://www.odoo.com/#apps">...</a>


搭建
----

*Mac OSX*

* [Mac下快速搭建Odoo10开发环境](http://www.mamicode.com/info-detail-2178388.html), [postgresql下载](https://www.postgresql.org/download/macosx/)
* [Odoo开发教程(一):使用pycharm搭建开发调试环境](https://blog.csdn.net/feigamesnb/article/details/50392082)
* [mac下完全卸载postgresql的方法](https://blog.csdn.net/stk_tianwen/article/details/17757393)


*Linux*

配置
----

* 更改监听端口

```
--xmlrpc-port=8070
```

* [PG 字符集设置](https://blog.csdn.net/sardden/article/details/43732307)

* 其他命令

```
locale -a | grep zh_CN

psql -U odoo -d postgres
```

[字符编码](https://blog.csdn.net/huoyunshen88/article/details/41113633)
-------

UTF-8 是编码方式，

en_US.UTF-8 和 zh_CN.UTF-8 是语言环境，也就是字符集

en_US.UTF-8 和 zh_CN.UTF-8 包含的字符数量是基本上一样的，大概是七万个汉字,编码都是 UTF-8 编码，字符集是 Unicode。


linux系统的语言环境设置成：export LANG=zh_CN.UTF-8，代表中国人使用的unicode字符集


en_US.UTF-8：你说英语，你在美国，字符集是utf-8
zh_CN.UTF-8：你说中文，你在中国，字符集是utf-8

如果你的LANG环境变量是en_US.UTF-8，那么系统的菜单、程序的工具栏语言、输入法默认语言就都是英文的。
如果你的LANG环境变量是zh_CN.UTF-8，那么系统的菜单、程序的工具栏语言、输入法默认语言就都是中文的。

问题集
-----

* [输入pip命令报错：from pip import main ImportError: cannot import name 'main'](https://blog.csdn.net/qq_38522539/article/details/80678412)

* [手动安装py依赖包]()

```
1. 使用pip 安装时，有时会遇到网上慢或者撞墙的现象，这时我们就到这个网站手动下载你需要的安装包：http://www.lfd.uci.edu/~gohlke/pythonlibs/。

2. pip install D:\Downloads\opencv_python-3.1.0-cp35-cp35m-win_amd64.whl

```

* [eucCN是什么](https://blog.csdn.net/qq_27361945/article/details/80780215)

```
在FreeBSD 4.11中，国际化、本地化支持中有个设置locale的细节，对于简体中文环境，很多的资料都推荐使用zh_CN.eucCN这个locale。
```

```
结论，eucCN就是GB2312,在FreeBSD 4.11中，已经不存在GB2312这个locale，eucCN就是GB2312，使用8位的两字节编码
```

* [locale的设定及其LANG、LC_ALL、LANGUAGE环境变量的区别](https://www.cnblogs.com/dolphi/p/3622420.html)

```
locale把按照所涉及到的文化传统的各个方面分成12个大类，这12个大类分别是： 

1、语言符号及其分类(LC_CTYPE) 
2、数字(LC_NUMERIC) 
3、比较和排序习惯(LC_COLLATE) 
4、时间显示格式(LC_TIME) 
5、货币单位(LC_MONETARY) 
6、信息主要是提示信息,错误信息,状态信息,标题,标签,按钮和菜单等(LC_MESSAGES) 
7、姓名书写方式(LC_NAME) 
8、地址书写方式(LC_ADDRESS) 
9、电话号码书写方式(LC_TELEPHONE) 
10、度量衡表达方式 (LC_MEASUREMENT) 
11、默认纸张尺寸大小(LC_PAPER) 
12、对locale自身包含信息的概述(LC_IDENTIFICATION)。
```

```
locale 是国际化与本土化过程中的一个非常重要的概念
```

