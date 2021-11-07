.. _ann_vararg:

@vararg Variable number of arguments annotation
-----------------------------------------------

.. note::

    Use ``@vararg`` to annotate variable number of arguments of a function 

* Full format

::

    ---@vararg TYPE

* Example

    .. code-block:: lua

        ---@vararg string
        ---@return string
        local function format(...)
            local tbl = { ... } -- inferred as string[]
        end