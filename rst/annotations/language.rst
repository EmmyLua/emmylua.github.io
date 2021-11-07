.. _ann_language:

@language Language injection
----------------------------

.. note::
    Use ``@language`` to inject syntax highlight to a piece of text

* Full format

::

---@language LANGUAGE_ID

* Example

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1

        ---@language JSON
        local jsonText = [[{
            "name":"Emmy"
        }]]

* Screenshot

.. image:: /images/annotation/language_injector.png
