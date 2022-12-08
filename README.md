# Breathe Like You

## Contents
* [Introduction](#40)
* [Research Blog](#41)  
  * [Week 5](#42)
  * [Week 6](#43)
  * [Week 7](#44)
  * [Week 8](#45)


<h2 id="40">Introductinon</h2>
Breathe Like You is an interactive art installation that reflects the relationship between two people based on their breathing rate.  

We use two PIR sensors and two analogue sound sensors as inputs, two led rings and a speaker as outputs to help two people feel the state they are in when they breathe at the same frequency.

Here is a video of our project: https://youtu.be/TEn1UXd2_kI  

<h2 id="41">Research Blog</h2>
<h3 id="42">Week 5: Project Proposal</h3>
In the topic selection phase, we first sorted out the inputs and outputs that could be used, as follows.  
   
**Input:** temperature, distance, light sensitivity, pressure, infrared thermography, buttons, time data, etc.  
**Output:** changes in lights, object movement and rotation, changes in sound, visual screens, projection, etc.

### Brain Storm
#### Idea 1: Curtains of Homeland -from Yutian
As we have just come to live in London for a month or so, there is an eight hour jet lag between the UK and China. We thought about how we could use the installation to represent this distance in time and space from our family and friends. The idea was to use the time and light changes in China as input and transmit the data to London via the internet. And to create a curtain-like installation in London, where the arduino would control the oscillation of the cloth (using servos) and the lights based on the data from China. This breaks the 8-hour time difference and allows the audience to connect with their homeland on another level.
  
But given the difficulty, after we looked up the data we found it might be difficult to accomplish. So the idea was to collect time and light data only in London, with an 8-hour delay in data transmission to the cloth and lights, thus achieving a feeling of going back in time.
  
**Input:** time, distance, light sensitivity, temperature;  
**Output:** motor for making the fan, servo, light.

#### Idea 2 Women's Voices– from Yufei
We are also very interested in feminist related topics. As the female voice is often ignored, we would like to make a installation where the male eyes and ears close when a female voice is heard. Possibly making a face mask two ear muffs and controlling their opening and closing using several servos.  
  
**Input:** distance measurement, sound sensor; 
**output:** servos.  
  
However, the idea was abandoned in view of the difficulty of distinguishing whether the sound sensor was a female voice or not.

#### Idea 3
During the discussion, we thought that the relationship between two people was something to think about and would also bring more variation to the piece. It occurred to us that the breath and temperature of two people could be shared to feed a plant, but considering that the change in the plant might not be obvious, we gave up this idea
**Input: CO2 sensor, temperature sensor; **  
**Output : oxygen and water.**

#### Idea 4
At this time we are interested in human breathing, which we see as the emotional embodiment of silence. In life we rarely pay attention to breathing, but a person's breathing is a certain reflection of the state he/she is in. When two people breathe at the same rate, are they able to approach each other's state of being, perceive each other's thoughts, or even share the same mind?
Considering that changes in feeding plants may not be visibly observable, we intended to look for other forms.   
We came up with Marina Abramović's The Artist Is Present: March - May 2010, a work whose form and the human relationships it discusses were of interest to us. We thought that when words are ignored, perhaps breathing can embody the interpersonal state.
We hoped that the work would encourage the participants to breathe in the same frequency, so we intended to set up a factor that would interfere when the pair did not breathe in the same frequency, and we came up with the idea of noise.

#### Final Proposal - Breathe Like You
(pdf link)
We decided to build a device that uses barometric and infrared sensors to calculate the participants' breathing rate and reflect it in the brightness of the lamp. The greater the difference between their breathing rates, the stronger the sound of the noise from the DC motor vibrations, prompting the pair to approach each other's breathing rates. The noise disappears when the pair breathes at the same frequency.  
（草图和电路图）
  
On 4 November we presented the proposal in class and Phoenix suggested that we test whether the air pressure sensor would work as we thought it would.![image]

<h3 id="43">Week 6</h3>
We bought two bmp180 air pressure sensors, two led rings, two PIR sensors from Amazon.  
<img width="280" alt="image" src="https://user-images.githubusercontent.com/119874724/206531756-cdf7025f-a3c6-41b6-90df-6ab85905688b.png">

We soldered the existing sensors after the delivery arrived.  
<img width="280" alt="image" src="https://user-images.githubusercontent.com/119874724/206529906-434ef63d-ec5f-4d73-9366-e96a2e5425f7.png">

When writing the code we found that each BMP180 needed a separate I2C code bus. We could not simply connect two sensors at the same time or switch between them, as that would block the I2C bus. It also has only one, unchangeable address.
After doing some research, we found that we could connect multiple BMP280s on the Arduino Uno via SPI, so we placed a new order for the BMP280.  
At this point, the code was initially completed.

<h3 id="44">Week 7</h3>
We designed the rough framework of the installation, which was to attach the air pressure sensor and PIR sensor to the horn, fix the horn to the shelf and make the stand for the installation out of PVC pipe. The installation will start working when the audience walks in.  
At the same time we would like to design a proper housing for the LED light rings.   
Option one would be to 3d print the lampshade and option two would be to fold the lampshade out of paper.  
Option one for the noise part is to use a wire tied to a DC motor. The wire makes noise by striking an object as it turns. The object material could be a plastic bag, a paper bag or a glass bottle, but of course this would need to be tested again. Option two is to make noise using the loudspeaker that we learnt about in week 6 of the lesson.
  
On Wednesday we downloaded 3d models of a lamp and a speaker and booked an intuction of 3d printing.  
<img width="680" alt="image" src="https://user-images.githubusercontent.com/119874724/206532451-beabc1e3-64a1-41b8-8e70-88c033dda457.png">

On Saturday we went to the 4d model shop in East London to buy the PVC pipes we needed, which did not look very good though. So instead we bought two microphone stands on Amazon that could be retracted in length. We also bought two funnels as plan B for the speakers in the shop, as well as blu tack and some wire.  
<img width="280" alt="image" src="https://user-images.githubusercontent.com/119874724/206552181-4eaadd65-0c4f-4f9a-9506-7c956b548a34.png">





