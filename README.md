# ComfyUI_Ultimate_SD_Upscale
Examples below are accompanied by a [tutorial in my YouTube video](https://youtu.be/FR5MlDPByA0).

This ComfyUI nodes setup lets you use [Ultimate SD Upscale](https://github.com/ssitu/ComfyUI_UltimateSDUpscale) custom nodes in your ComfyUI AI generation routine.

You can easily utilize schemes below for your custom setups. Simply save and then drag and drop relevant image into your [ComfyUI interface window](https://github.com/comfyanonymous/ComfyUI) with ControlNet Tile model installed, load image (if applicable) you want to upscale/edit, modify some prompts, press "Queue Prompt" and wait for the AI generation to complete. 

Stable Diffusion model used in this demonstration is [Lyriel](https://civitai.com/models/22922/lyriel?modelVersionId=72396).

Video tutorial on how to use ComfyUI, a powerful and modular Stable Diffusion GUI and backend, is [here](https://youtu.be/Ij8k6mBgL3o).

![ComfyUI_00214_](https://github.com/atdigit/ComfyUI_Ultimate_SD_Upscale/assets/105158639/6aea3273-b6a3-422a-b365-5c13a26b50fb)
![Clip_2](https://github.com/atdigit/ComfyUI_Ultimate_SD_Upscale/assets/105158639/86cf3ee5-89e9-4d9e-a4d0-1a22782fb972)
**↑ Node setup 1: Generates image and then upscales it with USDU (Save portrait to your PC and then drag and drop it into you ComfyUI interface and replace prompt with your's, press "Queue Prompt")**

![ComfyUI_00216_USDU_1 5x](https://github.com/atdigit/ComfyUI_Ultimate_SD_Upscale/assets/105158639/2ee4de6e-37c7-4fea-960a-faad2a18c92c)
![Clip_3](https://github.com/atdigit/ComfyUI_Ultimate_SD_Upscale/assets/105158639/ea61188a-37f3-4bd0-883d-8d5ec219d7c9)
**↑ Node setup 2: Upscales any custom image 3,5 times with USDU in delicate mode (Save portrait to your PC and then drag and drop it into you ComfyUI interface, drag and drop image you want to upscale to Load Image node and replace prompt with your's, press "Queue Prompt")**

![ComfyUI_00220_](https://github.com/atdigit/ComfyUI_Ultimate_SD_Upscale/assets/105158639/431c84f7-e04b-4da3-9b36-cdecc566ccea)
![Clip](https://github.com/atdigit/ComfyUI_Ultimate_SD_Upscale/assets/105158639/d86cee8a-e7a6-4ddb-9200-f2e589e2ddc2)
**↑ Node setup 3: Postprocess any custom image with USDU with no upscale: (Save portrait to your PC and then drag and drop it into you ComfyUI interface, drag and drop image you want to upscale to Load Image node and replace prompt with your's, press "Queue Prompt")**

You can use the [Official ComfyUI Notebook](https://colab.research.google.com/github/comfyanonymous/ComfyUI/blob/master/notebooks/comfyui_colab.ipynb) to run these schemas in Google Colab.
To successfully complete the above schemes add the following code to the above Colab notebook to the end of second (Checkpoints) cell:
<a name="example"></a>
```
!wget -c https://huggingface.co/comfyanonymous/ControlNet-v1-1_fp16_safetensors/resolve/main/control_v11u_sd15_tile_fp16.safetensors -P ./models/controlnet/

!wget -c https://huggingface.co/lokCX/4x-Ultrasharp/resolve/main/4x-UltraSharp.pth -P ./models/upscale_models/

!cd custom_nodes && git clone https://github.com/ssitu/ComfyUI_UltimateSDUpscale --recursive
