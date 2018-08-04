.. _ann_array:

array type
-----------------------------------

.. note::
    Use ``MY_TYPE[]`` to specify that a variable's type is an array type

* Full format:

::

---@type MY_TYPE[]

* Examples:

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1

        ---@type Car[]
        local list = {}

        local car = list[1]
        -- car. and you'll see completion

        for i, car in ipairs(list) do
            -- car. and you'll see completion
        end

.. seealso::
    :ref:`ann_type`