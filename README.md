# Computer-Vision-Deepmirror
The COCO data does not involve masks however the only stable modifyable maskrcnn i found asserted the presence of mask data in the target so I decided to use fasterrcnn. I had dozens of RAM and memory overloads so I will only train on 100 images using 10 epochs and batchsize of 1.
The finetuned model got trained on 100 images containing cats and dogs and managed to recognize the dog in the test image which is good enough. I used only the most confident box and label you can adjust that using the brackets below.

I managed to change the backbone without any modifications and make it work.

Then I created a class to multiply the last tensor of the backbone by a random number between 0.8-1.2 on the training step only but never managed to make it work and left as a further study to stick to 4 hours. I would expect the losses to decrease as this works as a good regularization technique. I will leave the code as a pseudo-ish code for demonstration.
Feel free to contact for any kind of execution problems.
