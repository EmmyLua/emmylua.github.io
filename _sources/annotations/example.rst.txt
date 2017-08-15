完整示例
-------------------

.. code-block:: lua
    :linenos:

    ---@class Transport @父类
    ---@public field name string
    local transport = {}

    function transport:move()end

    ---@class Car : Transport @Car继承自Transport
    local car = {}
    function car:move()end

    ---@class Ship : Transport @Ship继承自Transport
    local ship = {}

    ---@param type number @参数type说明
    ---@return Car|Ship @返回类型可能是Car也有可能是Ship
    local function create(type)
    -- 略
    end

    local obj = create(1)
    ---此时obj可代码提示

    ---@type Car
    local obj2
    ---此时obj2可代码提示

    local list = { obj, obj2 }
    ---@param v Transport
    for _, v in ipairs(list) do
    ---此时v可代码提示
    end