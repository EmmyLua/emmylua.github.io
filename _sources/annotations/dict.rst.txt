.. _ann_dict:

字典类型
-------------------

.. note::
    可以利用 ``table<KEY_TYPE, VALUE_TYPE>`` 的方式来标注一个数据类型为字典

* 完整格式：

::

---@type table<KEY_TYPE, VALUE_TYPE>

* 示例：

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1

        ---@type table<string, Car>
        local dict = {}

        local car = dict['key']
        -- car. 可以出现代码提示

        for key, car in pairs(dict) do
            -- car. 可以出现代码提示
        end

.. seealso::
    :ref:`ann_type`