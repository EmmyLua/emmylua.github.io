Attach Debug 附加调试
========================================

.. hint::
    说明：附加调试目前只能在 ``Windows`` 平台上使用，可以附加到32位和64位应用程序，因附加调试需将EmmyLua的调试模块 ``LuaInject.dll`` 注入到被调试程序进程中，一些杀毒软件、某卫士可能会弹窗报警告，如果注入过程被拦截则会出现注入失败的错误，导致调试失败。所以一定要选择放行或信任。

.. note::
    Attach Debug 目前处于实验阶段，不稳定。如果经常出现被调试程序崩溃的情况请改使用Remote方式调试。如若能提供重现崩溃BUG的工程是最好不过了

1. 执行步骤
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* 运行目标程序，打开IDEA菜单 ``Run`` -> ``Attach to Local Process...``

.. image:: /images/debug/attach-to-local-process.png

* 选择目标程序

.. image:: /images/debug/attach-with.png

*  注意控制台LOG，出现下图LOG表明附加成功

.. image:: /images/debug/attach-finish.png

* 然后就可以在源码中添加断点进行调试了

.. image:: /images/debug/attach-debug.png

2. 失败相关问题排查
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* 断点无效， IDEA控制台窗口出现 ``xxx not found`` 日志

::

    请确认 Sources 目录设置正确

* 附加到目标程序失败，出现 ``Error: LuaInject.dll could not be loaded into the process``

::

    检查是否被杀软、安全卫士拦截了注入过程