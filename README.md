# sp-configRabbitMq 常用命令及常见问题
原创Yumao_ 最后发布于2018-09-03 15:30:34 阅读数 2185  收藏
展开
管理概观 
        rabbitmqctl 是RabbitMQ中间件的一个命令行管理工具。它通过连接一个中间件节点执行所有的动作。本地节点默认被命名为”rabbit”。可以通过这个命令前使 用”-n”标志明确的指定节点名称, 例如: 
# rabbitmqctl -n rabbit@shortstop add_user tonyg changeit 
这个命令指示RabbitMQ中间件在rabbit@shortstop 节点创建一个tonyg/changeit的用户。 
在一个名为”server.example.com”的主机，RabbitMQ Erlang节点的名称通常是rabbit@server(除非RABBITMQ_NODENAM在 中间件启动时候被设置)。 
    hostnam -s 的输出通常是”@”符号正确的后缀。 
    rabbitmqctl 默认产生详细输出。通过”-q”标示可选择安静模式。 
    rabbitmqctl -q status 
应用和集群管理 
1.停止RabbitMQ应用，关闭节点 
# rabbitmqctl stop 
2.停止RabbitMQ应用 
# rabbitmqctl stop_app 
3.启动RabbitMQ应用 
# rabbitmqctl start_app 
4.显示RabbitMQ中间件各种信息 
# rabbitmqctl status 
5.重置RabbitMQ节点 
# rabbitmqctl reset 
# rabbitmqctl force_reset 
从它属于的任何集群中移除，从管理数据库中移除所有数据，例如配置过的用户和虚拟宿主, 删除所有持久化的消息。 
force_reset命令和reset的区别是无条件重置节点，不管当前管理数据库状态以及集群的配置。如果数据库或者集群配置发生错误才使用这个最后 的手段。 
注意：只有在停止RabbitMQ应用后，reset和force_reset才能成功。 
6.循环日志文件 
# rabbitmqctl rotate_logs[suffix] 
7.集群管理 
# rabbitmqctl cluster clusternode… 
用户管理 
1.添加用户 
# rabbitmqctl add_user username password 
2.删除用户 
# rabbitmqctl delete_user username 
3.修改密码 
# rabbitmqctl change_password username newpassword 
4.列出所有用户 
# rabbitmqctl list_users 

权限控制 
1.创建虚拟主机 
# rabbitmqctl add_vhost vhostpath 
2.删除虚拟主机 
# rabbitmqctl delete_vhost vhostpath 
3.列出所有虚拟主机 
# rabbitmqctl list_vhosts 
4.设置用户权限 
# rabbitmqctl set_permissions [-p vhostpath] username regexp regexp regexp 
5.清除用户权限 
# rabbitmqctl clear_permissions [-p vhostpath] username 
6.列出虚拟主机上的所有权限 
# rabbitmqctl list_permissions [-p vhostpath] 
7.列出用户权限 
# rabbitmqctl list_user_permissions username

通常我们谈到队列服务, 会有三个概念： 发消息者、队列、收消息者，RabbitMQ 在这个基本概念之上, 多做了一层抽象, 在发消息者和 队列之间, 加入了交换器 (Exchange). 这样发消息者和队列就没有直接联系, 转而变成发消息者把消息给交换器, 交换器根据调度策略再把消息再给队列。
————————————————
版权声明：本文为CSDN博主「Yumao_」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/p358278505/article/details/82349369
