# Stable_diffusion_GWEN
A "human in the loop" workflow for Stable Diffusion comparable to the Midjourney experience


## Sources
Stable diffusion : https://huggingface.co/CompVis/stable-diffusion-v1-4
Stable diffusion demo : https://colab.research.google.com/github/huggingface/notebooks/blob/main/diffusers/stable_diffusion.ipynb

Real ESRGAN : https://github.com/xinntao/Real-ESRGAN
Real-ESRGAN demo colab : https://colab.research.google.com/drive/1k2Zod6kSHEvraybHl50Lys0LerhyTMCo?usp=sharing

## Modifications

- Setting up a userfriendly version of the file with colab froms as GUI
- Setting up a three step image generation process to select the prefered picture and propose variations based on random Stable Diffusion parameters
- Linking the whole process with Real-ESRGAN 

## Why this modification

The workflow of Midjourney allows for randomness and paramers to generate alternatives to the prefered picture which can lead to serendipitiously generated pleasing productions.  So far this random slight variation part is not available (to my knowledge) in Stable diffusion and so I setup this to improve the workflow. Adding an implementation of Real-ESRGAN to complete the process. 

## Disclaimer
The same restrictions and warnings apply to this modified user experience ad to the orignial which can be found here : https://huggingface.co/CompVis/stable-diffusion-v1-4> 

## Colab file

