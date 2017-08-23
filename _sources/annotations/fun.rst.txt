.. _ann_fun:

函数类型
-------------------

.. note::
    可以利用 ``fun(param:MY_TYPE):void`` 的方式来标注一个数据类型为函数

* 完整格式：

::

---@type fun(param:MY_TYPE):RETURN_TYPE

* 示例：

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1, 7

        ---@type fun(key:string):Car
        local carCreatorFn1

        local car = carCreatorFn1('key')
        -- car. 可以出现代码提示

        ---@type fun():Car[]
        local carCreatorFn2

        for i, car in ipairs(carCreatorFn2()) do
            -- car. 可以出现代码提示
        end

.. seealso::
    :ref:`ann_type`