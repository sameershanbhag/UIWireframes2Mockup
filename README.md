# UIWireframes2Mockup
Solving a Computer Vision Problem of converting UI Wireframes to Mockups

# Training the Model

Go to CycleGanImpl

Open the Jupyter Notebook : Wireframe 2 Mockups - Training

Follow the Steps in the notebook

Note: Visdom server will be hosted on port **8051**

# For Testing

Open the Jupyter Notebook: Wireframe 2 Mockups - Testing

Follow the Steps

the output would be found in the Results folder

# Contents
Edge_Detected_Images_300_Images

Edge_Detected_Images_Complete_Dataset

Mockups_Complete_Dataset

Wireframes_Processed_200_Images

Wireframes_Original_Complete_Dataset

## Edge_Detected_Images_300_Images and Edge_Detected_Images_Complete_Dataset

We Used these images to train our first model. The output for this model was pretty amaizing.

Go To: UIWireframes2Mockup/Results/Edge_Detected_2_Mockup/Images
Lookout for: Files named Fake_B Results

Experiment Outcome: Just training for 20 - 25 Epoches the Output was prettu amaizing
Example Output:
![](https://ibb.co/RzGpTBQ)

## Mockups_Complete_Dataset

The Goal for our model.

## Wireframes_Processed_200_Images & Wireframes_Original_Complete_Dataset

We used this Images to train the second CycleGan Model to reach from Wireframes to Mockups. Th Results were not that great.

Wireframes_Original_Complete_Dataset contains more images as compared to Processed Images as it was difficult for some images to be cropped to keep the content only.

## Results

Contains two folders: 

1. Edge_Detected_2_Mockup : 

Contains training output for all 20 Epocs

2. Actual_Wireframe_Mockup : 

Used the above Trained model (Trained from Edge Detected Output) to Test it against our Hand Drawn Images. The Results were pretty awesomne but we are still facing some issue to get a clear output.


To See the Ouptut Look at the Images tagged with 'fake_b' in their name in the Images folder of Actual_Wireframe_Mockup in Results Directory

For any other Information please Directly contact:

Sameer Shanbhag (mailto:sshanbh1@uncc.edu)

Pranav Kamble (mailto:pkamble@uncc.edu)


