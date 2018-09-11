# 业务逻辑层


## 引用

```
from odoo import models, fields, api
```


## 用法


对于记录上的逻辑，使用@api.multi装饰器。

```
@api.multi 
def do_toggle_done(self): 
   for task in self: 
       task.is_done = not task.is_done 
   return True
```

用 @api.model装饰的方法上，自变量表示没有记录的模型。

```
@api.model 
def do_clear_done(self): 
   dones = self.search([('is_done', '=', True)]) 
   dones.write({'active': False}) 
   return True
```


## 解释

1.  该方法不需要返回任何东西，但我们应该让它至少返回一个True值。 原因是客户端可以使用XML-RPC来调用这些方法，并且此协议不支持只返回None值的服务器函数。
2. 