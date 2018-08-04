@field field annotation
-------------------

.. note::

    Use ``@field`` to add extra fields to an existing class (even it doesn't appear in your code)

* Full format:

::

    ---@field [public|protected|private] field_name FIELD_TYPE[|OTHER_TYPE] [@comment]

* Target:

    + After ``@class`` annotations

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 2
        
        ---@class Car
        ---@field public name string @add name field to class Car, you'll see it in code completion
        local cls = class()
        

.. seealso::
    :ref:`ann_class`