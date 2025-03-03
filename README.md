# NeuroSync Local API

### **22/02/2025 Half!!!**

Precision... for faster inference.

### **21/02/2025 Scaling UP! | New 228m parameter model + config added**

[Get the model on Huggingface](https://huggingface.co/AnimaVR/NEUROSYNC_Audio_To_Face_Blendshape/)

A milestone has been hit and previous research has got us to a point where scaling the model up is now possible with much faster training and better quality overall.

Going from 4 layers and 4 heads to 8 layers and 16 heads means updating your code and model, please ensure you have the latest versions of the api and player as the new model requires some architectural changes.

Enjoy!

### **19/02/2025 Trainer updates**

- **Trainer**: Use [NeuroSync Trainer Lite](https://github.com/AnimaVR/NeuroSync_Trainer_Lite) for training and fine-tuning.

- **Simplified Loss** Removed second order smoothness loss (left code in if you want to research the differences, mostly it just squeezes the end result resulting in choppy animation without smoothing)
- **Mixed Precision** Less memory usage and faster training
- **Data augmentation** Interpolate a slow set and a fast set of data from your data to help with fine detail reproduction, uses a lot of memory so /care - generally just adding the fast is best as adding slow over saturates the data with slow and noisey data (more work to do here... obv's!)


## 15/02/2025 update enables Rope + local/global positional encoding

Update your model from huggingface, or train a new one using rope and global/local positioning (set bools to true in model.py)

## NEW : [Train your own model](https://github.com/AnimaVR/NeuroSync_Trainer_Lite)

## 08/02/25 Open Source Audio2Face Model + code updates

The first version of the 0.02 model has been added. 

You MUST update all .py as the old ones wont work with the latest model (many changes involved in the model over this research period!)

## Talk to a NeuroSync prototype live on Twitch : [Visit Mai](https://www.twitch.tv/mai_anima_ai)

## Overview

The **NeuroSync Local API** allows you to host the audio-to-face blendshape transformer model locally. This API processes audio data and outputs facial blendshape coefficients, which can be streamed directly to Unreal Engine using the **NeuroSync Player** and LiveLink.

### Features:
- Host the model locally for full control
- Process audio files and generate facial blendshapes

## NeuroSync Model

To generate the blendshapes, you can:

- [Download the model from Hugging Face](https://huggingface.co/AnimaVR/NEUROSYNC_Audio_To_Face_Blendshape)
- [Apply for Alpha API access](https://neurosync.info) if you prefer not to host the model locally.

## Player Requirement

To stream the generated blendshapes into Unreal Engine, you will need the **NeuroSync Player**. The Player allows for real-time integration with Unreal Engine via LiveLink. 

You can find the NeuroSync Player and instructions on setting it up here:

- [NeuroSync Player GitHub Repository](https://github.com/AnimaVR/NeuroSync_Player)

Visit [neurosync.info](https://neurosync.info) for more details and to sign up for alpha access if you wish to use the non-local API option.
