# Audio Classification

Zero padding - If sample is shorter than uniform decided period os sample then the remaining part is covered by silence, that is called Zero Padding.

MFCC - used to recognize human voice 

Please refer the slides for detailed understanding

Now we will continue by creating an impulse.

You will get this window - 

![cevret](images/created.png)

Each one sec sample will be converted into image (13*49*1)

We will add MFCC by clicking on "add processing block"

Now we will select Keras framework for CNN classification 

Under "add a learnig block", we will select Classification, below you can see all the available learning blocks. 

![cevret](images/learning_block.png)

then we will save the impulse and below is the window picture after doing all this. 

<img width="1868" height="895" alt="image" src="https://github.com/user-attachments/assets/a3ba1c2d-b33a-4eec-b908-df0ee039fb5e" />

CNN architecture - extracted data is passed through CNN layers to extract features automatically 

Layers -> Flatten(Single dimension for decision making)-> Fully Connected -> FC -> Softmax

Input layer -> Reshaping -> CNN layer -> Dropout -> CNN layer -> Dropout -> Flattening -> Output layers

Data Augmentation - generating multiple variants of the same data point by changing color, angle of a picture

Now we jump on MFCC option on left menu column



Then we will train and evaluate, and we will get the confusion matrix



