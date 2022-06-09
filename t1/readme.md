# T1 - No check for Discovery TLV


## How long did it run?

## Did it find what we expected?
Yes - we expected to find a response with a missing tlv due to the deletion,
```C++
VerifyOrExit(Tlv::FindTlvOffset(aMessage, Tlv::kDiscovery, offset) == kErrorNone, error = kErrorParse);
```
this should not be accepted.

## If no why?

## Could the test be improved somehow?
