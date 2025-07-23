# Tiny ML Audio Classification

AI is all about data so that machine can learn. 

We have to use "Edge Impulse"

Refer slides for better understanding 

First, we are collecting the audio data through the hardware by using mic and ESP32 and SD card, but we can do this with laptop too.

To record this with hardware we can use the Arduino code provided in the codes folder

The audio samples I have recorded been provided in the images section

Then we have to upload the data on EdgeImpulse, and we can split as seen in the image because the each sample is 10 sec and we have 3-5 sec of important part, rest is useless. 

![csdc](images/spliting.png)

After spliting the data, we will get a non uniform dataset which is not goot to use. Now we will get a train/test split warning, because it is non uniform. 

![mkcewr](images/before.png)

so here, if we do "perform train/test split, then we will get fairly uniform data

![cewkjnc](images/after.png)

Then we do feature extraction and labelling and cleaning of data is done, in short, making it ready to use.

Now the training and rest of the part will be done in next day.


