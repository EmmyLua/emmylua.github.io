.. _ann_vararg:

@vararg 不定参数注解
-----------------------

.. note::

    使用 ``@vararg`` 注解一个函数的不定参数部分的类型

* 完整格式:

::

    ---@vararg TYPE

* 示例

    .. code-block:: lua

        ---@vararg string
        ---@return string
        local function format(...)
            local tbl = { ... } -- inferred as string[]
        end