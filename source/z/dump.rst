#############
Dump Analysis
#############

****
IPCS
****

IPCS Subcommands
================

如何执行?
---------
进入IPCS的ISPF UI后,有两种方法可以执行IPCS命令

#. 主菜单中进入 ``6 COMMAND``. 这里同时有一个常用命令的表格可以参考.
#. 在任意窗口的主命令行里输入::

    IPCS command parameters

   其中, ``IPCS`` 可以使用缩写 ``IP``. 子命令的缩写格式可以参照上述菜单中的表格.

Subcommands
-----------

LIST/LI
^^^^^^^
``IPCS LIST address ASID(x'asid') [LEN]GTH(lengh) [I]nstruction``
    列出 *asid* 地址空间里, 从 *address* 开始的 *length* 个字节. Instruction参数表示同时显示这些字节的反汇编结果.


SUMMARY/SUMM
^^^^^^^^^^^^
``IPCS SUMMARY FORMAT``
    详细的显示DUMP时的运行信息.

SYSTRACE
^^^^^^^^
``IPCS SYSTRACE ASID(X'asid') **UNIT** (x'') LOCAL``
    只显示指定的SYSTRACE. 其中 ``UNIT`` 可以是TCB/SRB的地址, 表示CPU的调度单位.

RUNCHAIN
^^^^^^^^
``RUNCHAIN ADDRESS(aabbccdd) LINK(0:3) EXEC((LIST X LEN(50)))``
