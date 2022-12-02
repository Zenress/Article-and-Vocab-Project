# Notes on the AI1 198

This files if here to describe and talk about the different reasons and speculations for why the initial setup did not succeed

## Login

Make sure the virtual machine is on

Click connect -> Select SSH and follow instructions there

## Logout

Command: logout

## How it was done

This section is meant to describe what we did.

We basically followed the steps on the spatial analysis page from Microsoft

https://learn.microsoft.com/en-us/azure/cognitive-services/computer-vision/spatial-analysis-container?tabs=virtual-machine

Warnings noticed:

From Xshfo1806-VirtualMachine-EdgeDevice_$edgeHub_Logs.txt

- <4> 2022-11-30 12:54:08.560 +00:00 [WRN] - Empty edge hub configuration received. Ignoring...
- <4> 2022-11-30 12:54:09.450 +00:00 [WRN] - Overriding address(es) '"http://+:80"'. Binding to endpoints defined in "UseKestrel()" instead.

Solution ideas:

- Update the configuration file for the IoT Hub
