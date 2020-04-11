# UI Wireframes to High-Fidelity Mockups

<br>

## About 
What problem are we trying to solve?

Most of the time, the websites that get drawn on whiteboards get changed during either the design phase or the development phase. The reason being the designers can't picture how the websites would actually look from the drawings, and they would modify the designs as they create them. The developers, on the other hand, would have to wait until the designers finalize the design and start coding the site from scratch. If the designers could visualize the designs better in real-time, they could finalize a design quickly. And if the final design can be easily converted to code then this makes the developers' job easy.

<br>

What is the problem statement we scoped?

This problem seemed worth solving & through Computer Vision we created a solution. We are hoping it would aid in the software development cycle, helping designers and developers save a lot of time and energy, and get to work on improving the product rather than starting from the ground up. To make this happen, we divided the project into two steps. First, we generate website-like images from whiteboard drawings. Then from the website-like images, we generate code. 

<br>

What is the solution we found?

The challenge was to create actual website-like images from the whiteboard drawings. We used a technique called CycleGAN to do this. CycleGAN is good at transferring the style of one image to another. In our problem, wireframes would be one domain of images and the actual website images would be another. What’s wonderful about CycleGAN is the images don’t have to be paired with each other. That is, we can have random whiteboard images and random actual website images as input data. 

Consider a scenario in which you are a language translator. If you translate an English phrase to French, you should be able to translate from French back to English and get the original phrase back. And it should work the other way as well - French to English to French. CycleGAN uses this concept to make sure it learns how to translate between wireframes and websites. 

We faced quite a few challenges to make CycleGAN work. CycleGAN is an expensive process. It requires large amounts of time and computational power. Initially, it wasn’t producing website images for the whiteboard images we gave, because it did not know what features to look for. So, we helped it out a little bit by first telling it what to look out for by highlighting the important features. Then, when we gave the whiteboard images it was able to produce good website images out of it. We had to vigilantly monitor its performance to stop it before the outputs became meaningless. We tried different options within CycleGANs to see how they perform and picked the optimal solution.

Pix2Code creates a skeleton code from website images. Pix2code uses high-resolution website images paired with the code for the images. We teach pix2code to produce skeleton code from website images. We use the website images generated by CycleGAN as inputs to pix2code to get our website skeleton. Currently, we are unable to produce meaningful code from the website images we’ve generated as they do not meet the resolution requirements of pix2code. We are planning to solve the resolution problem by a process called upsampling which increases the resolution of images. 



<br>
<br>

## Training the Model

Go to CycleGanImpl

Open the Jupyter Notebook : Wireframe 2 Mockups - Training

Follow the Steps in the notebook

Note: Visdom server will be hosted on port **8051**

<br>

## For Testing

Open the Jupyter Notebook: Wireframe 2 Mockups - Testing

Follow the Steps

the output would be found in the Results folder

<br>

## Folders
Edge_Detected_Images_300_Images

Edge_Detected_Images_Complete_Dataset

Mockups_Complete_Dataset

Wireframes_Processed_200_Images

Wireframes_Original_Complete_Dataset

<br>

#### Edge_Detected_Images_300_Images and Edge_Detected_Images_Complete_Dataset

We Used these images to train our first model. The output for this model was pretty amaizing.

Go To: UIWireframes2Mockup/Results/Edge_Detected_2_Mockup/Images
Lookout for: Files named Fake_B Results

Experiment Outcome: Just training for 20 - 25 Epoches the Output was prettu amaizing
Example Output:
![](https://ibb.co/RzGpTBQ)

<br>

#### Mockups_Complete_Dataset

The Goal for our model.

<br>

#### Wireframes_Processed_200_Images & Wireframes_Original_Complete_Dataset

We used this Images to train the second CycleGan Model to reach from Wireframes to Mockups. Th Results were not that great.

Wireframes_Original_Complete_Dataset contains more images as compared to Processed Images as it was difficult for some images to be cropped to keep the content only.

<br>

## Results

Contains two folders: 

1. Edge_Detected_2_Mockup: 

Contains training output for all 20 Epocs

2. Actual_Wireframe_Mockup: 

Used the above Trained model (Trained from Edge Detected Output) to Test it against our Hand Drawn Images. The Results were pretty awesomne but we are still facing some issue to get a clear output.


To See the Ouptut Look at the Images tagged with 'fake_b' in their name in the Images folder of Actual_Wireframe_Mockup in Results Directory

<br>

## Support

Contact us at: 

[Sameer Shanbhag](mailto:sshanbh1@uncc.edu)

[Pranav Kamble](mailto:pkamble@uncc.edu)

[Janani Arunachalam](mailto:jarunach@uncc.edu)

