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

The workflow of Midjourney allows for randomness and reroll / variations to generate alternatives of the prefered picture which can lead to serendipitiously generated pleasing productions.  So far these random slight variations are not available (to my knowledge) in Stable diffusion without loosing the seed or proceeding to manual variations and so I setup this to propose an open alternative to the MJ workflow. I added an implementation of Real-ESRGAN to complete the process with upscaling. Moreover, it seems important to provide a way to generate pictures without constant human supervision to avoid human timeloss. Through the proposed process, one can generate multiple pictures and keep only those fitting the criteria rather than repeating generation. It relies on automated captation of the seed and generation parameters to later-on propose slight or large variations based on user choice leading to a Midjourney-like experience.

## Workflow example 

### 1. Prompt definition
   "Photo of a beautiful Canadian landscape during the fall in the style of Erik McRitchie, high dynamic range"

### 2.First generation

The algorythm runs n steps (here 25) and random guidance between 0 and 10 (keeping the guidance variability low for now) and generated 2 to 8 pictures. Here 4 different pictures. The variations are marked and random in seed and guidance. We can imagine increasing higher the guidance but through my tests, it seems above 20, it turns into random noise and higher risk of flagged content.

![First Generation](https://github.com/ABBEN4/Stable_diffusion_GWEN/blob/main/pictures/set%201.png?raw=true)

## 3. Second generation from picture 3 - Low variation

The second generations saves the favourite picture and proceeds to variations which can be set manually or through presets (low, moderate, high, very high variation). Here with low variation preset. The differences are very minutes akin to changes is certain hues, very small shapes or rendering.

![Second Generation](https://github.com/ABBEN4/Stable_diffusion_GWEN/blob/main/pictures/lowvariation.png?raw=true)

## 3.Second generation from picture 3 - moderation variation

Here with moderate variation presets. More marked changes.

![Second Generation bis](https://github.com/ABBEN4/Stable_diffusion_GWEN/blob/main/pictures/moderateVariations.png?raw=true)


## 3.Second generation from picture 3 - Very high variation

Here with very high variation presets. The picture can be quite different but remains similar as it derives from the same seed.

![Second Generation bis](https://github.com/ABBEN4/Stable_diffusion_GWEN/blob/main/pictures/veryHigh.png?raw=true)


## 4.Final upscale

Real ESRGAN not performing as well as expect on certain outputs. Experimenting with other tools required and optimization with realESRGAN necessary possibly through smaller size input (resize to 30% of current output)

![Final](https://github.com/ABBEN4/Stable_diffusion_GWEN/blob/main/pictures/Scales.png?raw=true)

## Disclaimer
The same restrictions and warnings about bias apply to this modified user experience and workflow to the orignial Stable Diffusion which can be found [here](https://huggingface.co/CompVis/stable-diffusion-v1-4>) and real ESRGAN that can be found [here](https://github.com/xinntao/Real-ESRGAN). Please use this tool with caution and responsably. 

## File

The file available here was updated on : 

## Notes

Why GWEN ? Seemed to the logical counter part to MJ. 

