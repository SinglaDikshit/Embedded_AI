# Audio Classification

Zero padding - If sample is shorter than uniform decided period os sample then the remaining part is covered by silence, that is called Zero Padding.

MFCC - used to recognize human voice 

Please refer the slides for detailed understanding

## Creating an Impluse

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

## MFCC

Now we jump on MFCC option on left menu column

After that a new windoe will open there, we have to click on "autotune parameters" as we dont know about setting of parameters and then we have to save the parameters.

<img width="1853" height="905" alt="image" src="https://github.com/user-attachments/assets/e28956c2-042d-4ec2-a5c5-5a70450d9bf4" />

After auto tuning we will get this window and we have to click on Click on "Generate features"

<img width="1770" height="840" alt="image" src="https://github.com/user-attachments/assets/ab638bdf-f848-4ed6-bdf7-b96ac19bdf2a" />

These is the result - we have got the features 

<img width="1867" height="871" alt="image" src="https://github.com/user-attachments/assets/c9c0b5fa-a68d-4108-b454-010feb39a10f" />

## Classfier

Now, we will jump to the classifier section 

we see these layers 

Layers -> Flatten(Single dimension for decision making)-> Fully Connected -> FC -> Softmax

Input layer -> Reshaping -> CNN layer -> Dropout -> CNN layer -> Dropout -> Flattening -> Output layers

This is the window that we will get, and now you have to click on Train.

<img width="1840" height="935" alt="image" src="https://github.com/user-attachments/assets/94b8248f-10f6-4ee2-9fef-17414ec32945" />

Now, we will train and evaluate, and we will get the confusion matrix

<img width="876" height="726" alt="image" src="https://github.com/user-attachments/assets/704167ae-59a1-4cfa-84de-ca3d5cb4760a" />

<img width="882" height="642" alt="image" src="https://github.com/user-attachments/assets/d78a51ad-6cb0-4571-976f-4b3be75027c3" />

After this we can retrain it too but it is optional 

then we will go to Live classification but for that we have to connect a devide so we will skip

Next is model testing, we can click on classify all. 

Find the results below and note that I have got accuracy of 90.9 % having one mismatch

<img width="1808" height="890" alt="image" src="https://github.com/user-attachments/assets/1d576947-9125-4bc4-8504-3ff00f65aa7e" />

after we can do caliberation and deployemnt on hardware

for deployment, we can select "Arduino" library and go ahead with the process.

We will receive a ZIP file after building i have included that file in code section

<img width="1810" height="911" alt="image" src="https://github.com/user-attachments/assets/efd580a4-a0dd-4f86-ac91-d61e3b30eb60" />

We have to add this file to Arduino 

Use the source code provided in the slides to deploy in ESP using Arduino IDE

We can optimise parameters like mas_confidence if discrepancy in results
















