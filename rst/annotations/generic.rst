.. _ann_generic:

@generic Generic annotation
---------------------------

.. note::
    Use ``@generic`` to simulate ``generic`` in some high-level languages

* Full format

::

--@generic T1 [: PARENT_TYPE] [, T2 [: PARENT_TYPE]]

* Target

    + function

* Examples

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1,2,3,4,12

        ---@generic T : Transport, K
        ---@param param1 T
        ---@param param2 K
        ---@return T
        local function test(param1, param2)
            -- todo
        end
        
        ---@type Car
        local car = ...

        local value = test(car)

    .. image:: /images/annotation/generic.png