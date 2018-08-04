.. _ann_fun:

function types
-----------------------------------

.. note::
    Use ``fun(param:MY_TYPE):RETURN_TYPE`` to specify that a variable's type is a function type

* Full format

::

---@type fun(param:MY_TYPE):RETURN_TYPE

* Examples:

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1, 7

        ---@type fun(key:string):Car
        local carCreatorFn1

        local car = carCreatorFn1('key')
        -- car. and you see code completion

        ---@type fun():Car[]
        local carCreatorFn2

        for i, car in ipairs(carCreatorFn2()) do
            -- car. and you see completion
        end

.. seealso::
    :ref:`ann_type`