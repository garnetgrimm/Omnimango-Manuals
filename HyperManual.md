# Omnimango Hyper Series Manual
The Hyper Series consists of two unique plugins that are designed to work in tandum with each other. The first plugin, HyperLoop can be used to capture and loop an incoming signal, and optionally export them as wav files. One or multiple wav files can be then loaded into the HyperSyrup plugin and used as a wavetable. HyperSyrup can also load any regular wav file as well as preset wavetables from the popular Serum software.
## Hyperloop
![Looper](res/hyper-loop.png)  
This module listens to incoming audio data and loops the last few samples on command. This loop can be explorted to a wav file for use with HyperSyrup.
* **length** - the two knobs represent course and fine tuning for the length of the looped wave which is useful for capturing exact periods of incoming signals. The CV input can be used to modulate the length.
* **freeze** - continuously loop the previous number of samples specified by the length parameter until release.  This can be triggered by the switch or CV input. 
* **save** - export the selected wav to a wav file.
* **amplitude** - set the amplitude of the incoming signal.
* **in** - incoming audio
* **out** - outgoing (potentially looped) audio
## HyperSyrup
![Syrup](res/hyper-syrup.png)  
### Main Table
![Main Table](res/hyper-main-table.png)  
This table displays the general waveform constructed by the currently loaded waves.
#### Controls
![Main Controls](res/hyper-main-controls.png)  
* **z-pos** - select the tables current position in the z-axis
* **z-pos CV** - control how much the z-pos input will affect the overall position of the table in the z-axis
* **z-pos-input** - voltage control for the position of the table in the z-axis
* **unison** - how many oscillators are currently being used to play back the waveform. 
	* *WARNING: watch CPU% when using this*
* **detune** - how out of tune each oscillator allowed to be in relation to the main oscillator
* **v/oct** - polyphonic pitch control
* **gate** - polyphonic gate control
* **out** - monophonic output
### Editor Table
![Editor Table](res/hyper-editor.png)  
The editor table shows each wave in the table laid horizontally to make for easy manipulation. The controls for the table editor are listed below.
#### Controls
![Editor Controls](res/hyper-editor-controls.png)  
* **Select** - select a wave and subsequent transition frames from the editor table
* **Amplitude** - control the amplitude of the currently selected wave and subsequent transition frames
* **Length** -control the number of transition frames from the currently selected wave to the next wave in the editor
* **Wave** - open a single wav file and add it to the wave table.
* **Table** - open an entire previous table configuration into the wave table. This is compatible with wavetables the popular synth design plugin Serum.
* **Grab** - grab a selected wave from the editor table and move it to a new location.
* **Delete** - remove the selected wave
* **Save** - save the current wave table configuration as a wav table