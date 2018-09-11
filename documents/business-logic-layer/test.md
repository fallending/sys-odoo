# 测试



## 用法

业务逻辑添加测试

理想情况下，我们希望每行代码至少被一个测试用例覆盖到。在tests/test_todo.py文件中，向test_create（）方法再添加几行代码

```
 # def test_create(self):
        # ...
        # Test Toggle Done
        task.do_toggle_done()
        self.assertTrue(task.is_done)
        # Test Clear Done
        Todo.do_clear_done()
        self.assertFalse(task.active)
```


如果我们现在运行测试并且上面模型方法正确写入，那么我们在服务器日志中应该看不到错误消息：

```
$ ./odoo-bin -d todo -i todo_app --test-enable
```