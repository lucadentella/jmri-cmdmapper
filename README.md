# JMRI Command Mapper script

## Description
CmdMapper is a script for the model railway control software [JMRI](https://www.jmri.org/).
It's goal is to automatically *forward* turnout commands received from an interface to a different one.

It has been developed and tested for this setup:

 - Throttle network: **Loconet**
 - Command station: **DCC++**

Running this script you can control turnouts (using accessory decoders connected to DCC++) via Loconet devices (throttles, control panels...).

## Usage

First create the turnouts in JMRI  **Turnouts Table**:

![](https://github.com/lucadentella/jmri-cmdmapper/blob/main/turnouts.png?raw=true)

CmdMapper will forward incoming commands to a turnout with the same name (except the first letter which indicates the connection), for example:
|Source|Destination|
|--|--|
|LT1|DT1|
|LT2|DT2|
|...|...|
Then run the script (**Panels** - **Run Script...**).
A control panel is created, with two buttons to enable/disable the command mapping:

![](https://github.com/lucadentella/jmri-cmdmapper/blob/main/ctrlpanel.png?raw=true)

In the system console (**Help** - **System Console...**) it is possible to monitor the script activity:

![](https://github.com/lucadentella/jmri-cmdmapper/blob/main/sysconsole.png?raw=true)
