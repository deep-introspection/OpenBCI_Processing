# OpenBCI-GUI MOD. with OSC control
Edit the "selectedFreqBands.txt" file for defining your frequency bands of interest and related parameters.
See original [README.md](https://github.com/OpenBCI/OpenBCI_Processing) for more details about the GUI.

##Parameters:
- **fName (String)**: frequency band name
- **fStart (int)**: starting frequency bin
- **fEnd (int)**: final frequency bin (note that its a bin number and not the frequency)
- **Gain (float)**: multiplicative value of the average power
- **Min (float)**: minimum value of the normalized power
- **Max (float)**: maximum value of the normalized power

The final value **(Gain*Power-Min)/(Max-Min)** is sent by OSC to port 12000 at: /openbci/chan{channel number}/{frequency band name (i.e. fName)}

##Note:
- You can modify the Config file while the recording is running!!!
- Data acquisition is restarted every 10min. It's a temporary solution for encoutered unstable freeze of the recordings with the original GUI.

## Included:
- a PureData patch for DMX manipulation
- an OSCulator patch to monitor ongoing values

## Dependencies:
- oscP5
- netP5

## Contact/Questions:
Guillaume Dumas, deep[at]introspection.eu
