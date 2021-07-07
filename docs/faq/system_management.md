## 忘记了登录密码如何处理？

当普通用户忘记密码时可使用管理员账号在页面上的用户管理页面为其重置密码，当系统管理员忘记密码且没有其他系统管理员账号时，需要通过数据库操作重置密码。

MeterSphere 的用户信息存放在数据库中的 `user` 表中，其中 password 字段为用户密码的 `md5` 值。

```sql
update user set password='3259a9d7f208ef9690025d1432558c5b' where id='admin';
```

连接到数据库后，执行上面的 SQL 语句可以将用户 `admin` 的密码重置为 `metersphere`。

## 性能测试中，测试资源池的概念是什么？

资源池是指性能测试中所使用的发压服务器的集合。


