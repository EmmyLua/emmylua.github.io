.. _ann_class:

@class class declaration annotation
-------------------

.. note::
    EmmyLua use ``@class`` to simulate classes in OOP, supporting inheritance and fields

    .. image:: /images/annotation/class1.png

* Full format:

::

--@class MY_TYPE[:PARENT_TYPE] [@comment]

* Target:

    + local variables
    + global variables

* Examples:

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1

        ---@class Car : Transport @define class Car extends Transport
        local cls = class()

        function cls:test()
        end

* Descriptions:

    Sepcifies variable ``cls`` is class ``Car``, so we can use ``@type`` to specify other variables' types as Car, which can improve completion and other functionality.

.. seealso::
    :ref:`ann_type`