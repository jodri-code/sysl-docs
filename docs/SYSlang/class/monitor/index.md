## [SYSlang's Monitor](https://docs.pipewarp.co.uk/SYSlang/)

# The 'Monitor' Class
### huh, pc go broom

## Class Description
The 'Monitor' Class is designed to help smoothen out the hiccups in SYSlang's GUI's.

Due to the way SYSlang is currently set up, no other OS supports SYSlang Scripts other than SYStemware. Thanks to this _huge_ inconvenience, the Monitor class was created.

Monitor is essentially a mini-lib that provides Hardware Acceleration support.

## Class Imports
To import this class into your GUI based app or GUI based OS, use `require monitor`. This class is a part of SYSlang's Core Code, so it doesn't need to be imported as a lang asset.

## Some Definitions
- `monitor` calls `self()`. Use this to indicate to SYSlang that you are referencing this import.
- `setResourceLevel(auto|high|low)`. Sets the resource level usage.