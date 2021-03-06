# Emokit_Epoc_GUI

A GUI using PyQtGraph and Emokit library to plot PSD and raw data in real time from Emotiv Epoc

### Prerequisites

```
Python 2.7
Emokit python library - https://github.com/openyou/emokit
PyQt4.8+
pyqtgraph
scipy
```
Emokit library currently supports EPOC and some versions of EPOC+ 
I used EPOC in Ubuntu 16.04, but it should work also on Windows

### Usage

Just connect EPOC and run Epoc_GUI.py

Inside the script you can select which sensors will be plotted, the window size in which fft is calculated and the rate in which the plot is updated.

My first intention was to visualize data from 4 sensors maximum (8 graphs). If more sensors are selected then the graphs become very small and not very usefull.

In the time domain graphs there is an indicator of the quality of the signal, and also the color of the curve changes depending on the quality - from red (0) to green (>5100)

In the PSD graphs for every sensor there is an indicator of the peak frequency in every window.

Finally a butterworth bandpass filter is used to remove DC offset and 50Hz(or 60Hz) noise

![alt text](https://i.imgur.com/4ZdgbWB.png)
Using O1 and O2 sensors. O1's quality is 589 so the curve color is close to pure red, while O2's quality is closer to green (0,255,0).

![alt text](https://i.imgur.com/hG0S4co.png)
In this screenshot P7 is also added, however I have not connect its pad so the quality is 11, and also the PSD is very small (check the vertical PSD axes)

![alt text](https://i.imgur.com/InsIMgC.png)
Here is a screenshot while I had closed eyes, resulting strong alpha waves around 10.5Hz. 

## Authors

* **Christodoulos Benetatos** 

