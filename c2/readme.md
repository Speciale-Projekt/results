# C2 - Removed OT_ASSERT in WriteBytes


## How long did it run?

## Did it find what we expected?
Commented out in WriteBytes
```C++
    OT_ASSERT(aOffset + aLength <= GetLength());
```

## If no why?

## Could the test be improved somehow?
