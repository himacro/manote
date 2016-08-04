iPython
=======

环境变量
--------

    %env ENV value # 设置ENV为value
    %env ENV=value # 同上
    %env ENV       # 返回ENV的值

与系统shell的交互
-----------------

    var = !ls -l   # ls -l的结果讲义list的形式储存在var中

    pyvar = 'hello' # python 变量
    !echo "A python variable: {pyvar}" # 引用python变量
    !echo "A python variable: ", $pyvar # 引用python变量
