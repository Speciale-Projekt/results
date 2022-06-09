# C1 - A small dev mistake


## How long did it run?
```C++    
aMessage.MoveOffset(header.GetLength() - 1); // before
aMessage.MoveOffset(header.GetLength());     // after
```

## Did it find what we expected?

## If no why?

## Could the test be improved somehow?
