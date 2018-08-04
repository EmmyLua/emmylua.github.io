.. _ann_type:

@type type annotation
--------------------

.. note::
    Use ``@type`` annotation to specify the type of the target variable, to improve completions and other functionality.

    .. image:: /images/annotation/type1.gif

* Full format:

::

  ---@type MY_TYPE[|OTHER_TYPE] [@comment]


* Target:

    + local variables

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1, 4

        ---@type Car @instance of car
        local car1 = {}

        ---@type Car|Ship @transport tools, car or ship. Since lua is dynamic-typed, a variable may be of different types
        ---use | to list all possible types
        local transport = {}

    + global variables

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1
        
        ---@type Car @global variable type
        global_car = {}

    + properties

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 2

        local obj = {}
        ---@type Car @property type
        obj.car = getCar()

.. seealso::
    :ref:`ann_class`