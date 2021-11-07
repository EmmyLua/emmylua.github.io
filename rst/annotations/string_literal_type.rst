.. _ann_string_literal_type:

String literal type annotation
------------------------------

.. note::

    Use String literal type to specify a fixed string.
    Combined with the ``@alias`` this can be used simulate "enumeration" 


* Example

    .. code-block:: lua

        ---@alias Handler fun(type: string, data: any):void

        ---@param event string | "'onClosed'" | "'onData'"
        ---@param handler Handler | "function(type, data) print(data) end"
        function addEventListener(event, handler)
        end

    .. image:: /images/annotation/string_literal_types_1.png

    |

    .. image:: /images/annotation/string_literal_types_2.png

    |

    .. note::

        It is recommended to use ``@alias`` to simplify type complexity

    .. code-block:: lua

        ---@alias Handler fun(type: string, data: any):void

        ---@alias IOEventEnum string | "'onClosed'" | "'onData'"

        ---@param event IOEventEnum
        ---@param handler Handler | "function(type, data) print(data) end"
        function addEventListener(event, handler)
        end

    .. image:: /images/annotation/string_literal_types_3.png