# Lua

## Numbers

```lua
-- Integer examples
local a = 10
local b = -5

-- Floating-point examples
local c = 3.14
local d = -0.001

-- Arithmetic operations
local sum = a + c        -- 10 + 3.14 = 13.14
local difference = b - d -- -5 - (-0.001) = -4.999
local product = a * d    -- 10 * (-0.001) = -0.01
local quotient = c / b   -- 3.14 / (-5) = -0.628

-- Printing results
print("Sum:", sum)               -- Output: Sum: 13.14
print("Difference:", difference) -- Output: Difference: -4.999
print("Product:", product)       -- Output: Product: -0.01
print("Quotient:", quotient)     -- Output: Quotient: -0.628
```

## Redis

Redis Server supports Lua scripting.

---

For logging, use this code as reference to print different levels of messages inside a Lua script:

```lua
local function debug_print(msg)
    redis.log(redis.LOG_WARNING, msg)
    redis.log(redis.LOG_NOTICE, msg)
    redis.log(redis.LOG_DEBUG, msg)
    redis.log(redis.LOG_VERBOSE, msg)
end
```

The lower the number, the more verbose the message. Also, log level(s) above the one used will also be covered. E.g.

- if `LOG_NOTICE` is used, `LOG_WARNING` is covered.
- Similarly, if `LOG_DEBUG` is used, `LOG_WARNING`, `LOG_NOTICE` are covered.
- Similarly, if `LOG_VERBOSE` is used, `LOG_WARNING`, `LOG_NOTICE`, `LOG_DEBUG` are covered.

---
