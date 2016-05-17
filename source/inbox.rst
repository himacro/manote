#######
Inbox
#######


Atom's per-project settings
   * 暂时用 project manager解决，等待官方功能上线

ltrace和strace
    * ltrace 追踪动态库的调用
    * strace 追踪syscall的调用

逆火效应(Backfire Effect)
    * 当人们遇上与自身信念相抵触的观点或证据时，除非它们足以摧毁原信念，否则会忽略或者反驳它们，而原信念反而更加强化．
    * (可能原因) 新信息威胁到了接受者的自我认知,从而产生负面情绪.而负面情绪阻碍我们的认知和理解能力, 从而影响了对新信息的消化.

添加自己的Rexx库
    * 系统会从SYSEXEC, SYSPROC这两个DD里寻找Rexx命令. 要添加自己的Rexx库, 就需要添加到这两个DD上. 通常选择SYSEXEC.
    * 执行下面的TSO命令添加自己的Rexx库:
        * ``TSO ALTLIB DEACTIVATE APPLICATION(EXEC)``
        * ``TSO ALTLIB ACTIVATE APPLICATION(EXEC) DATASET('your.rexx.lib')``
