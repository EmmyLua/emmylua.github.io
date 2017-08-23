.. _ann_array:

数组类型
-------------------

.. note::
    可以利用 ``MY_TYPE[]`` 的方式来标注一个数据类型为数组

* 完整格式：

::

---@type MY_TYPE[]

* 示例：

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1

        ---@type Car[]
        local list = {}

        local car = list[1]
        -- car. 可以出现代码提示

        for i, car in ipairs(list) do
            -- car. 可以出现代码提示
        end

.. seealso::
    :ref:`ann_type`