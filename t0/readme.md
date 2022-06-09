# T0 - No version TLV
We removed the Version TLV as a requirement for Parent Request,
if OT responds our Statemachine should pick it up and report it as an error.


## How long did it run?
It ran from Monday the 06/06-2022 @ 10:31:22 till Thursdag the 09/06-2022 @ 10:47:15


## Did it find what we expected?
No


## If no why?
To find this error the AFLnet needed to mutate a totally correct message except that the VersionTLV was not a part of it. The ods of that is astronomically small.

## Could the test be improved somehow?
If we could somehow tell AFLnet how the message structure is, we could make it fuzz on the an individual TLV level instead of on all of the message in total.
Lets say we want the following:
00 FF 11 22 33 44 55 66 77 88 99 10 01 04 12 32 12 32 07 02 55 33
This can be broken down into the following parts:
Security header:
00
AUX security header
FF 11 22 33 44 55 66 77 88 99 10
Command Type:
01
First TLV:
01 04 12 32 12 32
Second TLV:
07 02 55 33

Even the TLV's could be seperated into their components.
This would make us able to do regular blacbox fuzzing, by yeeting different compleatly random messages into the OT application, but it would also allow us to do messages that is formated correctly.

