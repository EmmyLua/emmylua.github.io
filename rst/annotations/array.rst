.. _ann_array:

Array type annotation
-----------------------------------

.. note::
    Use ``MY_TYPE[]`` to specify that a variable's type is an array type

* Full format

::

---@type MY_TYPE[]

* Examples

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1

        ---@type Car[]
        local list = {}

        local car = list[1]
        -- start typing car. and you'll see the completion

        for i, car in ipairs(list) do
            -- start typing car. and you'll see the completion
        end

.. seealso::
    :ref:`ann_type`