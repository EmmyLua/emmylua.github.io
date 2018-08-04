.. _ann_dict:

table type
-------------------

.. note::
    Use ``table<KEY_TYPE, VALUE_TYPE>`` to specify that a variable's type is a table(a.k.a. dictionary, map) type

* Full format:

::

---@type table<KEY_TYPE, VALUE_TYPE>

* Examples:

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1

        ---@type table<string, Car>
        local dict = {}

        local car = dict['key']
        -- car. and you'll see completion

        for key, car in pairs(dict) do
            -- car. and you'll see completion
        end

.. seealso::
    :ref:`ann_type`