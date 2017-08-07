.. _ann_class:

@class类声明注解
-------------------

.. note::
    EmmyLua利用 ``@class`` 注解来模拟面向对象中的类，可以继承，可以定义字段/属性

* 完整格式

::

--@class {my_type}[ : parent_type] @comment string

* 应用目标：

    + local 变量
    + global 变量

* 示例：

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1

        ---@class Car : Transport @定义一个Car类继承父类Transport
        local cls = class()

        function cls:test()
        end

* 示例说明：

    将 ``cls`` 变量标记为 ``Car`` 类，在其它地方可以使用 ``@type`` 注解来标记目标变量类型，以增强代码提示以及其它功能

.. seealso::
    :ref:`ann_type`