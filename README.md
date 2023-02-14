
# Classification of Diffusion Model Generated Images

As part of this project we have built a CNN model, using transfer learning approach , that can distinguish between AI generated art (created using AI-powered tool Dall.E) and original art created by artists. 

## Problem:

Identify if the image in question is an original artwork or if it was generated by Dall.E. 

## Context: 

With the rise of AI-powered tools, we are faced with the ethical concern of the originality of a creative endeavor. Additionally, AI generated media could potentially cause discourse if it refers to polarizing topics, which we have seen play out with exceptionally realistic deepfakes. Dall.E uses texutual prompts to generate images, using its own extensive library of original art created by human artists, which begs the questions-" who really is the owner of the new art?","are the original artists credited for the new art created using their pieces?","what happens to the creatives if the AI takes over and does their job?","Will there be a loss of appreciation for the artists around us?". Along with this AI has also been used to generate fraudulent art and with the rise of investments in NFTs, to determine the authenticity of a digital piece, we find ourselves with a very opportune usecase where this project is useful.

## Impact:

With this project we plan to help differentiate between an original artwork and AI generated art which would help people and companies wanting to own a piece of art, know about its authenticity. An extrapolation of this project is detecting deepfakes in images as well as video frames.

## Approach:

For this we created a custom dataset where we used the Dall.E api to generate 600+ images using varying random prompts. For the Original artwork we programatically pulled the images (600+) using a list of urls from The Paintings Dataset (https://www.robots.ox.ac.uk/~vgg/data/paintings/ ) curated by Elliot J. Crowley, Ernesto Coto and Andrew Zisserman.
For modelling we used a pre-trained Resnet-18 model for feature extraction and fine tuned it with the data that we gathered.
We decided to use Accuracy as as metric as our dataset was no imbalanced and the cost of the prediction is not severe (as per the usecase and the stakes defined we may pivot to using some other metric to determine how the model is doing or for hyper parameter tuning). We did however capture the confusion matrix metrics for every model we ran.
We wanted to expose a public api and make this app accessible to anyone who wants to try it but doesnt care to run any scripts. That is why we hosted our app on Hugging Face and deployed it using gradio for easy UI navigation. 

## Limitations:

Since the model was trained on images generated using Dall.E, it is able to weed out those AI- generated images better as it learns the patterns/signature that Dall.E uses. We would like to enhance this model by feeding it images from a wide variety of AI-powered image generation tools

## User guide:

User can access the app through the link-https://huggingface.co/spaces/NehaBardeDUKE/ComputerVision_540 . This takes the user to a public space on hugging face where they can drop an image in the input box as prompted and they will get the prediction along with the probability of the prediction. We chose to add this in order to provide the user with explanability of the result.
https://user-images.githubusercontent.com/110474064/218609768-ea63be4d-7f1c-42ff-a4c2-e99ddb15f909.mp4

## Training Data:


## Training Procedure:

## Evaluation Results:
### Deep learning Model
### Non-Deep learning Model

## Citations






