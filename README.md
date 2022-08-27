# Stable_diffusion_GWEN
A "human in the loop" workflow for Stable Diffusion comparable to the Midjourney experience


## Sources
[Stable diffusion](https://huggingface.co/CompVis/stable-diffusion-v1-4)
[Stable diffusion demo](https://colab.research.google.com/github/huggingface/notebooks/blob/main/diffusers/stable_diffusion.ipynb)

[Real ESRGAN](https://github.com/xinntao/Real-ESRGAN)
[Real-ESRGAN demo colab](https://colab.research.google.com/drive/1k2Zod6kSHEvraybHl50Lys0LerhyTMCo?usp=sharing)

## Modifications

- Setting up a userfriendly version of the file with colab froms as GUI
- Setting up a three step image generation process allowing the selection of the prefered picture and proposing variations based on random Stable Diffusion parameters settings
- Solving RAM saturation to ensure the generation process
- Linking the whole process with Real-ESRGAN to allow for endpoint upscaling


## Why this modification

The workflow of Midjourney allows for randomness and reroll / variations to generate alternatives of the prefered picture which can lead to serendipitiously generated pleasing productions.  So far this random slight variation part is not available (to my knowledge) in Stable diffusion and so I setup this to propose an open alternative to this workflow. I added an implementation of Real-ESRGAN to complete the process with upscaling. Moreover, it seems important to provide a way to generate pictures without constant human supervision to avoid human timeloss. Through the proposed process, one can generate multiple pictures and keep only those fitting the criteria rather than repeating generation. It relies on automated captation of the seed and generation parameters to later-on propose slight or large variations based on user choice leading to a Midjourney-like experience.

## Workflow example 

**Prompt :**      "Nature and humans in harmony, artwork, painting by Johanesse Dugas"

**First generation**

![First Generation](https://github.com/ABBEN4/Stable_diffusion_GWEN/blob/main/pictures/Image-1.png?raw=true)

**Second generation**


![Second Generation](https://github.com/ABBEN4/Stable_diffusion_GWEN/blob/main/pictures/SecondGeneration.png?raw=true)


## Disclaimer
The same restrictions and warnings about bias apply to this modified user experience and workflow to the orignial Stable Diffusion which can be found [here](https://huggingface.co/CompVis/stable-diffusion-v1-4>) and real ESRGAN that can be found [here](https://github.com/xinntao/Real-ESRGAN). Please use this tool with caution and responsably. 

## File

The file available here was updated on : 

## Notes

Why GWEN ? Seemed to the logical counter part to MJ. 

