## [SYSlang's Monitor](https://docs.pipewarp.co.uk/SYSlang/class)

# The 'Monitor' Class
### huh, pc go boom

## Class Description
The 'Monitor' Class is designed to help smoothen out the hiccups in SYSlang translations and to smoothen out the GUI interfaces and how SYStemware runs.

Due to the way SYSlang is currently set up, no other OS supports SYSlang Scripts other than SYStemware. Thanks to this _huge_ inconvenience, the Monitor class was created.

Monitor is essentially a mini-lib that provides Hardware Acceleration support.

## Class Imports
To import this class into your GUI based app or GUI based OS, use `require monitor`. This class is a part of SYSlang's Core Code, so it doesn't need to be imported as a lang asset.

## Lib Definitions
- `monitor` calls `self()`. Use this to indicate to SYSlang that you are referencing this import.
- `setResourceLevel(auto|high|low)`. Sets the resource level usage. Possible options are auto, high or low. Low is not equal to a battery saver, and high is not equal to a gamer mode, the same as how auto will most likely just set it to high and leave it as so.

### [Return](https://docs.pipewarp.co.uk/SYSlang/class)
