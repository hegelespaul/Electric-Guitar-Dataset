<!--# Electric Guitar Dataset

A repository for showing advances on a dataset aimed for Deep Learning using different electric guitar sounds.

Pd is used to do data augmentation by running sampled electric guitar recorded thru D.I. into different sound presets of Amplitube, a demo of this process can be seen on the .mp4 file in this repository

![An example of a TSNE of some datapoints](https://i.ibb.co/cC3YpqT/Muestra.jpg)

-->
To create the database we used 5 seconds length normalized audio recordings of all the possible notes in a standard tuning electric guitar of 22 frets processed through 12 different guitar effects. Trying to cover up the most used guitar pickups, we employed two different kinds of electric guitars, one with a dual-coil 3-way pickup selector and another one with a single coil 5-way pickup selector. To be precise, a 1978 Japanese Ibanez Performer PF300 (it’s considered a high-quality Ibanez clone of a Gibson Les Paul) with 0.10 to 0.46 string gauges and a 2004 American Stratocaster with 0.9 to 0.42 mm string gauges respectively. Both guitars were recorded with volume and tone knobs at max position being the strings plucked by a 2mm. Dunlop plastic pick in a middle position between the end of the fretboard and the beginning of the bridge. The Stratocaster had a string height going from 2.5 to 3.0 mm and the PF300 from 1.5 to 2.0 mm, both measures from the first to the sixth string and both guitars were tuned and calibrated with new strings only played before the recordings for calibration purposes.

The effects used included analog gear with and without digital components and were picked up by popularity and type. Our main goal was to use popular effects and try to cover up different years of production and types of guitar effects. We divided the effects in four categories: gain, modulation, delay, and reverb, and used three different types of effect per category.

The controls of the effects varied form one another, but our approach was to use 100%  wet signal of the effects at 100\% of its intensity, meaning that the distortion, depth and range knobs were dialed all the way up; the tone parameters of the pedals were remained in a flat position and those parameters involving a time related control like speed or rate, were manually set to match a quarter note in a 120 bpm time. In the case of the the delay tones, because the delayed sound did not aligned with the rest of the audios generated, we combined the wet signal with the dry one in a 50-50% proportion.

## Gain

TubeScreamerMini: A compact version of the iconic TS-808 Saturation effect from Ibanez. The pedal used was made in Japan in 2019. 

RAT2: A Proco’s very popular distortion pedal, the one used had the serial number erased but by its components and design we deduced that was a later 2010 model made in China by Neutrik.

BD-2: A widely used overdrive pedal from Boss Company. The version used is a 2018 model made in Taiwan and has the same schematic as their first Blues Driver pedal released in 1995.

## Modulation

CE-3: A Chorus Pedal made in Japan in 1987 by Boss. It includes, at its time, a ground-breaking stereo configuration, but we only used the mono one.

Phase45: A MXR phaser pedal made from 1977 to 1981, its a simplified one knob version of their well known phaser pedal Phase90, the one used was build in U.S.A. in 1980.

E-Lady: A Mooer clone of the Electric Mistress, an iconic flanger pedal from 1975 made by Electro-Harmonix. The pedal used was made in China in 2022, it features a filter mode that stops the flanger phase shift, but we only used the normal mode that imitates the functionality of the Electric Mistress.

## Delay

DL4: A delay stomp box unique in its kind when introduced into the market in 1999. This digital emulator of 16 different type of delays remained unmodified for nearly 23 years. Of the 16 possible delays we only used three, Tape Echo, Sweep Echo and Digital Delay. The first one is an emulation of the Maestro Ecoplex 3, a solid-state tape delay created in 1972, and the other two where line 6’s own approaches to digital delays using 24-bit depth resolution, the Sweep Echo took the Echoplex 1 as base model but with the addition of a sweep filter thought the repetitions of the delay and the Digital Delay was a state of the art true stereo delay, but in this case, as in all the effects used, we only took into account the mono version of the effect. The pedal used is a Line 6 2007 model made in China.

## Reverb

CR6OC: We used a digital reverb emulations of an Orange Crush Pro 60  12-inch speaker combo amplifier, the main reason was to introduce in some way the color of an amplifier and mainly, to do a common practice for getting reverb in the tone of a guitarist, we could have used different digital or analog reverb gears, but its sounding would have differ from the ones used in a live guitar scenario and would have been closer to a very dedicated studio tone, contrasting in one way with our latent space that is created only by mono recordings and with our main intention on comparing commonly used guitar effects with the results obtained of that latent space. The amplifier used is a 2014 model made in China and the reverberations it integrates are Plate, Hall and Spring digital emulations.

The methodology used for recording consisted in these two simple steps:

1. We did a recording of the guitar sounds through the direct input of the audio interface.

2. We then took the recorded guitar notes and processed using the outputs of the interface as the input of the effects and then we connected the outputs of the effects to the inputs of our interface, making a round loop with a small latency compensated in the DAW.

The interface used is an Audient ID 14.

---

Here is an ilustration of the gear used:


|![Gear Used](https://i.ibb.co/jrNVLsS/Pedales.jpg)|
|![Gear Used](https://i.ibb.co/PYHPyGP/Guitarra.jpg)|

---


The relations of the audio currently recorded can be seen here:


<iframe src="https://docs.google.com/spreadsheets/d/18XRDFhlTCr_tPlikjZ1wQdlvKLkLAYCD/edit?usp=sharing&ouid=104576609693167581701&rtpof=true&sd=true" style="border:0px #ffffff none;" name="myiFrame" scrolling="yes" frameborder="1" marginheight="0px" marginwidth="0px" height="800px" width="1280px" allowfullscreen></iframe>


---
Here you can see PCA's of the currently recorded audios and the visualizations of the advances of a variable autoencoder created from the recordings:


<iframe src="visual_pca.html" style="border:0px #ffffff none;" name="myiFrame" scrolling="yes" frameborder="1" marginheight="0px" marginwidth="0px" height="800px" width="1280px" allowfullscreen></iframe>
