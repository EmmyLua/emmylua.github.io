.. _ann_language:

@language内嵌语言
-------------------

.. note::
    可以利用 ``@language`` 的方式来标注一段文本为某种代码格式，从而可以显示高亮

* 完整格式：

::

---@language LANGUAGE_ID

* 示例：

    .. code-block:: lua
        :linenos:
        :emphasize-lines: 1

        ---@language JSON
        local jsonText = [[{
            "name":"Emmy"
        }]]
        
* 效果：

.. image:: /images/annotation/language_injector.png
