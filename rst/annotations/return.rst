@return Function return type annotation
---------------------------------------

.. note::

    Use ``@return`` to specify the return type of a function

    .. image:: /images/annotation/return1.gif

* Full format

::

    ---@return MY_TYPE[|OTHER_TYPE] [@comment]

* Target

    + functions
    
    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1

        ---@return Car|Ship
        local function create()
            ...
        end

        ---Here car_or_ship doesn't need @type annotation, EmmyLua has already inferred the type via "create" function
        local car_or_ship = create()
    
    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1

        ---@return Car
        function factory:create()
            ...
        end
