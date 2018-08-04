.. _ann_generic:

@generic 泛型注解
-------------------

.. note::
    利用 ``@generic`` 注解来模拟高级语言中的 ``泛型``

* 完整格式

::

--@generic T1 [: PARENT_TYPE] [, T2 [: PARENT_TYPE]]

* 应用目标：

    + function

* 示例：

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1,2,3,4,12

        ---@generic T : Transport, K
        ---@param param1 T
        ---@param param2 K
        ---@return T
        local function test(param1, param2)
            -- todo
        end
        
        ---@type Car
        local car = ...

        local value = test(car)

    .. image:: /images/annotation/generic.png