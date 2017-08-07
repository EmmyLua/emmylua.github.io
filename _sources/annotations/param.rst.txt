@param参数类型标记注解
-----------------------------------

.. note::

    利用 ``@param`` 注解来标记函数定义参数的类型，以增强代码提示以及其它功能

* 完整格式：

::

    ---@param {param_name} {my_type}[|other_type] @comment string

* 应用目标：

    + 函数参数
    + for循环参数

* 示例：

    .. code-block:: lua
        :linenos:

        ---@param car Car
        local function setCar(car)
        end
    .. code-block:: lua
        :linenos:

        ---@param car Car
        for k, car in ipairs(list) do
        end