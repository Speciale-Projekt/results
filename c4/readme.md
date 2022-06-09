# C4 - removed isvalid on DiscoveryRequest


## How long did it run?

## Did it find what we expected?
removed the outer if statment in HandleDiscoveryRequest
````c++
    if (discoveryRequest.IsValid())
{
    ...
}
````

## If no why?

## Could the test be improved somehow?
