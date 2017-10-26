@field 属性注解
-------------------

.. note::

    利用 ``@field`` 注解来标记某个类的额外的属性（即使这个属性没有出现在代码里）

* 完整格式：

::

    ---@field [public|protected|private] field_name FIELD_TYPE[|OTHER_TYPE] [@comment]

* 应用目标：

    + 在 ``@class`` 注解之后
    
    .. code-block:: lua
        :linenos:
        :emphasize-lines: 2
        
        ---@class Car
        ---@field public name string @标记Car有一个name属性，代码提示中会出现相应提示
        local cls = class()
        

.. seealso::
    :ref:`ann_class`