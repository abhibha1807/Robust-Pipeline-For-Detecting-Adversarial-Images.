# Robust-Pipeline-For-Detecting-Adversarial-Images.

Deep learning has fueled great strides in a variety of computer vision problems, such as object detection, action recognition, human pose estimation, and segmentation. Despite there success, research has shown that DNN's are broadly vulnerable to adversarial examples, carefully chosen inputs that cause the network to change output without a visible change to a human. Yet, for humans these perturbations are often visually imperceptible. In fact, so called adversarial examples are crucially characterized by requiring minimal perturbations that are quasi-imperceptible to a human observer. Keeping this in mind, we propose a robust pipeline capable of detecting adversarially attacked images

## Pipeline
The pipeline consists of 3 steps. First is generating adversarially attacked images using different attacking methods (FGSM, PGD and Patch based attack) from the ILSVRC 2012 dataset . Next, we pass the generated samples through Mantranet that identifies perturbations and stores manipulation masks of the image. Finally a binary classifier is trained on the manipulation masks to differentiate between real and fake images.

<img width="401" alt="Screenshot 2021-11-06 at 4 16 57 PM" src="https://user-images.githubusercontent.com/34295094/140606914-69095ec3-70ca-4446-9319-c687b92906f4.png">

## Results
<img width="574" alt="Screenshot 2021-11-06 at 4 22 45 PM" src="https://user-images.githubusercontent.com/34295094/140607047-ee5b761e-b089-499a-8e6b-bd3af816345c.png">

## Examples

1. Example of FGSM attack
<img width="592" alt="Screenshot 2021-11-06 at 4 26 44 PM" src="https://user-images.githubusercontent.com/34295094/140607147-09a80ad6-cf91-4d2d-8c1c-32aa816bcabc.png">

2. Example of Patch attack
<img width="540" alt="Screenshot 2021-11-06 at 4 29 48 PM" src="https://user-images.githubusercontent.com/34295094/140607199-1ef4ee78-ab07-4b1a-9e79-22b6985bc151.png">


3. Example of PGD attack
<img width="675" alt="Screenshot 2021-11-06 at 4 28 33 PM" src="https://user-images.githubusercontent.com/34295094/140607185-986a097c-31bc-4dac-bcbc-ddd27cf7101f.png">

## Dataset

https://image-net.org/challenges/LSVRC/2012/
