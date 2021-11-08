# Computer-Vision-Deepmirror

The only stable and modifyable version of maskrcnn i found, asserted the presence of mask data as a target variable so I decided to use faster-rcnn instead of mask-rcnn. I had dozens of times of RAM and memory overloads so I decided to only train on 100 random images from COCO including cats, using 10 epochs and small batches. I used only the most confident box and label, you can adjust that using the brackets in the training.

I managed to change the backbone as "resnet" without any modifications and make it work.

Then I created a class to multiply the last tensor of the backbone by a random number between 0.8-1.2 on the training step only but never managed to make it work and left as a further study to stick to 4 hours. I would expect the losses to decrease as this works as a good regularization technique. I will leave the code as a pseudo-ish code for demonstration.

The idea for this modification is to seperate the backbone, tell the model that the prior layers do not need grads, add a linear transformation layer to the end of it which multiplies each tensor with a random float between 0.8-1.2 and place this backbone back inside the R-CNN.

I recommend using the fiftyone session tool for visualizations. Feel free to contact for any kind of execution problems.
