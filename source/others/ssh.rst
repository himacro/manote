###
SSH
###

*********
公钥推送
*********
命令```ssh-copy-id`` 可以将生成的公钥推送到主机上

************************
配置连接共享和长连接配置
************************
配置文件: ``* ~/.ssh/config``.

连接共享配置::

    ControlMaster auto
    ControlPath /tmp/ssh_mux_%h_%p_%r

长连接(即使所有客户端关闭, 也在一定时间内保持连接)::

    ControlPersist 4h  # 长连接
