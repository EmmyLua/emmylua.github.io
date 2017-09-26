.. _ann_type:

@type类型标记注解
--------------------

.. note::
    利用 ``@type`` 注解来标记目标变量的类型，以增强代码提示以及其它功能

* 完整格式：

::

  ---@type MY_TYPE[|OTHER_TYPE] [@comment]


* 应用目标：

    + local 变量

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1, 4

        ---@type Car @汽车的实例
        local car1 = {}

        ---@type Car|Ship @交通工具，车或者船。因lua脚本的灵活性，一个变量可能对应多个类型，
        ---用|符号列出可能的类型
        local transport = {}

    + global 变量

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1
        
        ---@type Car @标记全局的变量类型
        global_car = {}

    + property 属性

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 2

        local obj = {}
        ---@type Car @标记属性的类型
        obj.car = getCar()

.. seealso::
    :ref:`ann_class`