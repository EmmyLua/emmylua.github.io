.. _ann_string_literal_type:

字面量类型
-----------------------

.. note::

    字面量类型（String literal types）允许你指定字符串作为固定的代码提示，结合 ``@alias`` 特性可以起到类似“枚举”的效果


* 示例

    .. code-block:: lua

        ---@alias Handler fun(type: string, data: any):void

        ---@param event string | "'onClosed'" | "'onData'"
        ---@param handler Handler | "function(type, data) print(data) end"
        function addEventListener(event, handler)
        end

    .. image:: /images/annotation/string_literal_types_1.png

       
    .. image:: /images/annotation/string_literal_types_2.png

    .. note::

        建议使用 ``@alias`` 简化类型复杂度

    .. code-block:: lua

        ---@alias Handler fun(type: string, data: any):void

        ---@alias IOEventEnum string | "'onClosed'" | "'onData'"

        ---@param event IOEventEnum
        ---@param handler Handler | "function(type, data) print(data) end"
        function addEventListener(event, handler)
        end

    .. image:: /images/annotation/string_literal_types_3.png