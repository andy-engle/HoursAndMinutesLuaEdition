## Hours and Minutes project lua edition

```lua
-- Andrew Engle
-- HoursAndMinutes

local MINUTES_PER_HOUR = 60 -- Define conversion constant.

while true do
    io.write("Enter time in minutes (-1 to Exit): ") -- Prompt the user.
    local input = io.read() -- Read user input.
    local minutes = tonumber(input) -- Convert input to number.

    if minutes then -- Check if conversion was successful.
        if minutes == -1 then
            break -- Terminate the loop if exit statement encountered.
        end

        local hours = math.floor(minutes / MINUTES_PER_HOUR) -- Calculate hours from minutes.
        local minutesLeftOver = minutes % MINUTES_PER_HOUR -- Calculate the remainder.

        -- Display output.
        print(string.format("%d minutes is %d hours and %d minutes", minutes, hours, minutesLeftOver))
    else
        -- Prompt the user to try again because conversion failed.
        print("Could not parse input, please try again!")
    end
end
```