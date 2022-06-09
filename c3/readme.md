# C3 - Removed Valid Header Check 


## How long did it run?

## Did it find what we expected?
Removed:
```c++
VerifyOrExit(header.IsValid() && header.GetLength() <= length, error = kErrorParse);
```
## If no why?

## Could the test be improved somehow?
