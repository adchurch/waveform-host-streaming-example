# waveform-host-streaming-example
## Overview
This example uses the VeriStand Host Waveform Streaming API to stream VeriStand DAQ waveforms to a host PC. The example writes the waveform data into a TDMS file and in parallel reads the synchronized wavefrom data back from the same TDMS file for display.   

## License
This project is intended as an example only and is distributed as open source code with the BSD-2 "Simplified" license. 

## Required Software
* NI VeriStand 2015 or later
* NI LabVIEW 2015 or later

## Required Hardware
* NI Real-Time target or Windows PC running VeriStand Engine
* Windows Host PC (or virtual machine)
* NI DAQ card. This can be any card supported by VeriStand's built-in DAQ functionality. This includes most DAQmx-based cards. It does not include DMMs or FPGA waveforms. 

## Included Files
* LabVIEW Project
* VeriStand Project 
* Both saved in 2015

## Instructions
1. Open *Waveform Host Streaming.nivsproj* file.
2. Open the System Explorer.
2. Update Controller IP address.
3. Update DAQ configuration to match the card type and alias you are using. Note the Waveforms paths (can be copied to clipboard from System Explorer) which will be used in the LabVIEW project.
4. Save the System Definition and deploy the project.
5. Open the Workspace and update the Waveform Chart channel configuration.
6. Open *Waveform Streaming Test.lvproj*. Open *Stream Waveforms.vi*. 
7. Update *Waveform Paths* control to match the waveforms you are streaming. 
8. Update *Log File Path* control to a directory where you have write access. 
9. Run the VI. This will trigger the waveform which is configured for a 40 second acquisition. This example only supports a single capture when the VI is first run. 
10. Use the *Samples to View* and *Offset* controls to change how much data is displayed in the chart and from what offset in the TDMS log.
10. Click the *Stop* control to stop the VI. 