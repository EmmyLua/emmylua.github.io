.. _ann_alias:

@alias Alias annotation
-----------------------

.. note::

    Use ``@alias`` to register complex types with a new name

* Full format

::

    ---@alias NEW_NAME TYPE

* Example

    .. code-block:: lua

        ---@alias Handler fun(type: string, data: any):void

        ---@param handler Handler
        function addHandler(handler)
        end