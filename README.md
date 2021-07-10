Example:

```local lbt = require("lbt")

local test_string = [[<Trigger name="Take Bandage" state="False" id="6"/>]]
local new = lbt.gsub(test_string, '<Trigger name="*s" state="*s" id="*s"/>', function(name, state, id)
    return 'Trigger name is ' .. name .. " state = " .. state:lower() .. " and id = " .. id
end)
print(new) ```
