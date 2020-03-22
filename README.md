# Audio Visualization Project
Creative Coding Lab  
Prof. Oliver Steele  
Spring 2020  

### Noise Art 
[ZEIT](https://my-project-march2020.now.sh)  
[Documentation Blog](https://wp.nyu.edu/kennedycambracho/)  

My work illustrates the dynamic nature of personal perception in relation to spatial audio. I use P5.js, the javascript library, and the surrounding ambient noise as input to create a real-time visual abstraction of spatial audio. This process mimics the experience of synesthesia where stimuli are incorrectly processed and perceived by an individual. My synthetic sensory experience offers users a chance to view the links formed between auditory input and visual output through abstract art.
What fascinates me about synesthesia is its relation to individual reality construction. Those who are diagnosed with synesthesia experience a separate reality. Their perceived world is so far removed from my understanding that simply imagining the experience is near impossible. With this project, I provide a lens to view an alternate sensorial reality.  

[Demo Video](youtube.com)
#### Pre-Production
Before begining the production process, I first reviewed the P5.js sound library as well as spent time researching audio analysis. Using this knowledge, I determined the FFT feature witin the sound library is how I would analyze the audio sample. 
#### Functionality
Using a sample mp3 file (found [here](https://freemusicarchive.org)), I began by looking at the array returned from `FFT.analyze()`. The array contains the measurements at a number of frequencies (default is 1024). 
By cutting the array down (changing the number of bins) and breaking it into various frequency ranges, I was able to have a single float represent a single, dynamic characteristic of the audio sample. This number is produced using `getEnergy(frequency)`. Here the frequency is defined as a string value: "bass", "lowMid" "mid", "highMid", and "treble". 
#### Design 
In order to convey the sense of environment, I chose to use WEBGL rederer. The 3D space allows the visualization to live within a world with depth; it mimics how the audio input exists within a dynamic environment where the space is not seperate from sound but intertwined with its production and perception. 
#### Reflection
If given more time, I would like to develop a more efficient visual language. This would facilitate users in identifying patterns and the subsequent information exchange. A successful visual language accurately conveys the audio input's characteristics while also presenting itself in such a way that users are able to interpret the meaning.

#### Resources 
[Spectrum Properties](https://www.gigahertz-optik.de/en-us/basics-light-measurement/light-color/spectr-line-properties/)

[P5.js Sound Library](https://p5js.org/reference/#/libraries/p5.sound)

[Coding Train](https://www.youtube.com/channel/UCvjgXvBlbQiydffZU7m1_aw)