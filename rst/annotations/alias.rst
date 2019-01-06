.. _ann_alias:

@alias 别名注解
-----------------------

.. note::

    可以使用 ``@alias`` 将一些复杂不容易输入的类型注册为一个新的别名

* 完整格式:

::

    ---@alias NEW_NAME TYPE

* 示例

    .. code-block:: lua

        ---@alias Handler fun(type: string, data: any):void

        ---@param handler Handler
        function addHandler(handler)
        end