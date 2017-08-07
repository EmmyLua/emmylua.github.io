@return 函数返回值注解
--------------------------------

.. note::

    利用 ``@return`` 注解来标记函数的返回值类型

* 完整格式：

::

    ---@return {my_type}[|other_type] @comment string

* 应用目标：

    + 函数

* 示例：

    .. code-block:: lua
        :linenos:

        ---@return Car|Ship
        local function create()
            ...
        end

        ---此时car_or_ship类型可以不用@type标记，EmmyLua已通过create函数的推断出了类型
        local car_or_ship = create()
    
    .. code-block:: lua
        :linenos:

        ---@return Car
        function factory:create()
            ...
        end
