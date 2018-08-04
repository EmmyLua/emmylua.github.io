@param parameter type annotation
-----------------------------------

.. note::

    Use ``@param`` to specify the types of function parameters, to improve completions and other functionality.

    .. image:: /images/annotation/param1.gif

* Full format:

::

    ---@param param_name MY_TYPE[|other_type] [@comment]

* Target:

    + function parameters

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1

        ---@param car Car
        local function setCar(car)
            ...
        end

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1

        ---@param car Car
        setCallback(function(car)
            ...
        end)

    + for loop variables

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1

        ---@param car Car
        for k, car in ipairs(list) do
        end