# OpenBCI-GUI MOD. with OSC control

Edit the "selectedFreqBands.txt" file for defining your frequency bands of interest (allow gain and min/max ajustement).
The OSC values are then sent to port 12000 at: /openbci/chan{channel name}/{frequency band name}
Notice that you can modify the Config file while the recording is running.

Every 10min, the data acquisition is restarted (temporary solution for unstable freeze of the recordings).

Included:
- a PureData patch for DMX manipulation
- an OSCulator patch to monitor ongoing values

Dependencies: requires oscP5 and netP5 librairies

Contact/Questions: Guillaume Dumas, deep[at]introspection.eu

See original [README.md](https://github.com/OpenBCI/OpenBCI_Processing) for more details about the GUI.
