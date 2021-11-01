# WaveRiding
 WaveRiding, consisting of a feature extractor and a wave-table audio-visual synthesiser. Both input and output devices have been developed in Max/MSP, implementing OSC, wavetable synthesis and Jitter for visuals. 

The inputcode is a regression-based feature extractor called WaveRider. It extracts the gyroscope data from the iPhone (pitch, roll, yaw) and sends them to Wekinator fro Machine Learning traning. 

The outputcode is Wavetable-VisualSynth; a wave-table audio-visual synthesiser developed in Max/MSP using real-time DSP and Jitter (visual-library). 
The synth is based on th.polar.wave~ and th.wave.table objects by Timo Hoogland

Machine Learning is used as a sound exploration method,  controlling 13 parameters of the synthesizer using my iPhone gyroscope (pitch, roll, yaw) via the Wekinator regression-based model. 
The algorithms used to train the regression-based model are Neural networks (NN)with 1 layer

- Instructions for compiling any associated inputs and/or outputs, including information about any external libraries that are required, or requirements on the operating system or hardware needed to run the project. 

For the WaveRider_input the cnmat external library is needed:
https://cnmat.berkeley.edu/downloads

For the Wavetable-VisualSynth th.polar.wave~ and th.wave.table objects by Timo Hoogland are needed:
https://github.com/tmhglnd/wave-terrain-synthesis

GyrOSC app :
https://www.bitshapesoftware.com/instruments/gyrosc/

System / Hardware needed :
iOS handset (developed and tested on iPhone12-iOS 14.8)

PC or Mac (developed and tested on Windows 10 and OSX 10.14.5) 

Max/MSP  (developed and tested on version 8.1) 

Any MIDI keyboard.

- Instructions for how to run and use your project. 

1.
Ensure that the following dependencies are installed.

Max/MSP
 cnmat external library is needed:
https://cnmat.berkeley.edu/downloads

th.polar.wave~ and th.wave.table objects by Timo Hoogland are needed:
https://github.com/tmhglnd/wave-terrain-synthesis

iOS
GyrOSC app :
https://www.bitshapesoftware.com/instruments/gyrosc/

Wekinator- Kadenze version
http://www.wekinator.org/kadenze/




2.
a.Open the WaveRider_input

b.Open the GyrOSC app on your end set. Type your IP address and make sure the port is set to 9999. From the bottom menu, select the second icon from the left. Turn the Gyroscope on and switch off everything else. Set Frequency to 60. 
Return to the IP address page by selecting the first icon from the left (bottom menu). Now you should see in yellow that only the {pitch, roll, yam} have been selected. You should now see these values within the WaveRider_input app in Max/MSP.

c. Open the WekinatorProject_waverider.wekproj. As a default this project will  listen on port 6448  and send on port 12000.
You should see the OSC in lead turn green when you interact with your hand set.

d. Open the Wavetable-VisualSynth_output file. Ensure that you select your audio- and midi device from Max/MSP Audio/ Midi preferences. Turn on the DSP from the bottom right corner of the app. Click  World On to start the rendering and synthesis on the Wavetable-VisualSynth. Send / play midi notes

e. Adjust the Wekinator sliders to morph/explore audio-visual presets. When you are happy interact with your handset to train your model/s

f. you can also sound design presets directly on the synthesiser. The parameters labelled in Wekinator will self- update. Also, you can store presets on the Wavetable-VisualSynth (left UI area) by shift+click to store and shift+alt+click to erase.
