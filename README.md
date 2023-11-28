<div align="center">
<h2>Animated-vedios-Generation-Crafting-Lifelike-3D-Talking-Faces-from-Static-Images-and-Sound</h2>

<!--<h2> Animated-vedios-Generation-Crafting-Lifelike-3D-Talking-Faces-from-Static-Images-and-Sound</span> </h2> -->


<div>
    <a target='_blank'>Adinarayana Thota </a>&emsp;
    <a></a></a>&emsp;
  
</div>
<br>


<br>


![sadtalker](https://user-images.githubusercontent.com/4397546/222490039-b1f6156b-bf00-405b-9fda-0c9a9156f991.gif)

<b>TL;DR: &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; single portrait image 🙎‍♂️  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;+  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; audio 🎤  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; =  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; talking head video 🎞.</b>

<br>

</div>



## Highlights

- The license has been updated to Apache 2.0, and we've removed the non-commercial restriction
- We've published research paper. 
- Full image mode is now available! [More details...](https://github.com/OpenTalker/SadTalker#full-bodyimage-generation)

| still+enhancer in v0.0.1                 | still + enhancer   in v0.0.2       |   [input image @bagbag1815](https://twitter.com/bagbag1815/status/1642754319094108161) |
|:--------------------: |:--------------------: | :----: |
| <video  src="https://user-images.githubusercontent.com/48216707/229484996-5d7be64f-2553-4c9e-a452-c5cf0b8ebafe.mp4" type="video/mp4"> </video> | <video  src="https://user-images.githubusercontent.com/4397546/230717873-355b7bf3-d3de-49f9-a439-9220e623fce7.mp4" type="video/mp4"> </video>  | <img src='./examples/source_image/full_body_2.png' width='380'> 

- Several new modes (Still, reference, and resize modes) are now available!



## To-Do

We're tracking new updates in [issue #280](https://github.com/OpenTalker/SadTalker/issues/280).

## Troubleshooting

If you have any problems, please read our [FAQs](docs/FAQ.md) before opening an issue.



### Linux/Unix

1. Install [Anaconda](https://www.anaconda.com/), Python and `git`.

2. Creating the env and install the requirements.
  ```bash
  git clone https://github.com/Animated-vedios-Generation-Crafting-Lifelike-3D-Talking-Faces-from-Static-Images-and-Sound.git

  cd SadTalker 

  conda create -n sadtalker python=3.8

  conda activate sadtalker

  pip install torch==1.12.1+cu113 torchvision==0.13.1+cu113 torchaudio==0.12.1 --extra-index-url https://download.pytorch.org/whl/cu113

  conda install ffmpeg

  pip install -r requirements.txt

  ### Coqui TTS is optional for gradio demo. 
  ### pip install TTS

  ```  
### Windows

A video tutorial in chinese is available [here](https://www.bilibili.com/video/BV1Dc411W7V6/). You can also follow the following instructions:

1. Install [Python 3.8](https://www.python.org/downloads/windows/) and check "Add Python to PATH".
2. Install [git](https://git-scm.com/download/win) manually or using [Scoop](https://scoop.sh/): `scoop install git`.
3. Install `ffmpeg`, following [this tutorial](https://www.wikihow.com/Install-FFmpeg-on-Windows) or using [scoop](https://scoop.sh/): `scoop install ffmpeg`.
4. Download the SadTalker repository by running `git clone https://github.com/Winfredy/SadTalker.git`.
5. Download the checkpoints and gfpgan models in the [downloads section](#2-download-models).
6. Run `start.bat` from Windows Explorer as normal, non-administrator, user, and a Gradio-powered WebUI demo will be started.

### macOS

A tutorial on installing SadTalker on macOS can be found [here](docs/install.md).

### Docker, WSL, etc

Please check out additional tutorials [here](docs/install.md).

## 2. Download Models

You can run the following script on Linux/macOS to automatically download all the models:

```bash
bash scripts/download_models.sh
```

We also provide an offline patch (`gfpgan/`), so no model will be downloaded when generating.

### Pre-Trained Models

* [Google Drive](https://drive.google.com/file/d/1gwWh45pF7aelNP_P78uDJL8Sycep-K7j/view?usp=sharing)
* [GitHub Releases](https://github.com/OpenTalker/SadTalker/releases)
* [Baidu ](https://pan.baidu.com/s/1kb1BCPaLOWX1JJb9Czbn6w?pwd=sadt) (Password: `sadt`)

<!-- TODO add Hugging Face links -->

### GFPGAN Offline Patch

* [Google Drive](https://drive.google.com/file/d/19AIBsmfcHW6BRJmeqSFlG5fL445Xmsyi?usp=sharing)
* [GitHub Releases](https://github.com/OpenTalker/SadTalker/releases)
* [Baidu ](https://pan.baidu.com/s/1P4fRgk9gaSutZnn8YW034Q?pwd=sadt) (Password: `sadt`)

<!-- TODO add Hugging Face links -->


<details><summary>Model Details</summary>


Model explains:

##### New version 
| Model | Description
| :--- | :----------
|checkpoints/mapping_00229-model.pth.tar | Pre-trained MappingNet in Sadtalker.
|checkpoints/mapping_00109-model.pth.tar | Pre-trained MappingNet in Sadtalker.
|checkpoints/SadTalker_V0.0.2_256.safetensors | packaged sadtalker checkpoints of old version, 256 face render).
|checkpoints/SadTalker_V0.0.2_512.safetensors | packaged sadtalker checkpoints of old version, 512 face render).
|gfpgan/weights | Face detection and enhanced models used in `facexlib` and `gfpgan`.
  
  

## 3. Quick Start

Please read our document on [best practices and configuration tips](docs/best_practice.md)

### WebUI Demos

**Online Demo**: [HuggingFace](https://huggingface.co/spaces/vinthony/SadTalker) | [SDWebUI-Colab](https://colab.research.google.com/github/camenduru/stable-diffusion-webui-colab/blob/main/video/stable/stable_diffusion_1_5_video_webui_colab.ipynb) | [Colab](https://colab.research.google.com/github/Winfredy/SadTalker/blob/main/quick_demo.ipynb)

**Local WebUI extension**: Please refer to [WebUI docs](docs/webui_extension.md).

**Local gradio demo (recommanded)**: A Gradio instance similar to our [Hugging Face demo](https://huggingface.co/spaces/vinthony/SadTalker) can be run locally:

```bash
## you need manually install TTS(https://github.com/coqui-ai/TTS) via `pip install tts` in advanced.
python app_sadtalker.py
```

You can also start it more easily:

- windows: just double click `webui.bat`, the requirements will be installed automatically.
- Linux/Mac OS: run `bash webui.sh` to start the webui.


### CLI usage

##### Animating a portrait image from default config:
```bash
python inference.py --driven_audio <audio.wav> \
                    --source_image <video.mp4 or picture.png> \
                    --enhancer gfpgan 
```
The results will be saved in `results/$SOME_TIMESTAMP/*.mp4`.

##### Full body/image Generation:

Using `--still` to generate a natural full body video. You can add `enhancer` to improve the quality of the generated video. 

```bash
python inference.py --driven_audio <audio.wav> \
                    --source_image <video.mp4 or picture.png> \
                    --result_dir <a file to store results> \
                    --still \
                    --preprocess full \
                    --enhancer gfpgan 
```

More examples and configuration and tips can be founded in the [ >>> best practice documents <<<](docs/best_practice.md).



## Acknowledgements

Facerender code borrows heavily from [zhanglonghao's reproduction of face-vid2vid](https://github.com/zhanglonghao1992/One-Shot_Free-View_Neural_Talking_Head_Synthesis) and [PIRender](https://github.com/RenYurui/PIRender). We thank the authors for sharing their wonderful code. In training process, we also used the model from [Deep3DFaceReconstruction](https://github.com/microsoft/Deep3DFaceReconstruction) and [Wav2lip](https://github.com/Rudrabha/Wav2Lip). We thank for their wonderful work.

We also use the following 3rd-party libraries:

- **Face Utils**: https://github.com/xinntao/facexlib
- **Face Enhancement**: https://github.com/TencentARC/GFPGAN
- **Image/Video Enhancement**:https://github.com/xinntao/Real-ESRGAN

## Extensions:

- [SadTalker-Video-Lip-Sync](https://github.com/Zz-ww/SadTalker-Video-Lip-Sync) from [@Zz-ww](https://github.com/Zz-ww): SadTalker for Video Lip Editing

## Related Works
- [StyleHEAT: One-Shot High-Resolution Editable Talking Face Generation via Pre-trained StyleGAN (ECCV 2022)](https://github.com/FeiiYin/StyleHEAT)
- [CodeTalker: Speech-Driven 3D Facial Animation with Discrete Motion Prior (CVPR 2023)](https://github.com/Doubiiu/CodeTalker)
- [VideoReTalking: Audio-based Lip Synchronization for Talking Head Video Editing In the Wild (SIGGRAPH Asia 2022)](https://github.com/vinthony/video-retalking)
- [DPE: Disentanglement of Pose and Expression for General Video Portrait Editing (CVPR 2023)](https://github.com/Carlyx/DPE)
- [3D GAN Inversion with Facial Symmetry Prior (CVPR 2023)](https://github.com/FeiiYin/SPI/)
- [T2M-GPT: Generating Human Motion from Textual Descriptions with Discrete Representations (CVPR 2023)](https://github.com/Mael-zys/T2M-GPT)

## Disclaimer

This is not an official product of Tencent. 

```
1. Please carefully read and comply with the open-source license applicable to this code before using it. 
2. Please carefully read and comply with the intellectual property declaration applicable to this code before using it.
3. This open-source code runs completely offline and does not collect any personal information or other data. If you use this code to provide services to end-users and collect related data, please take necessary compliance measures according to applicable laws and regulations (such as publishing privacy policies, adopting necessary data security strategies, etc.). If the collected data involves personal information, user consent must be obtained (if applicable). Any legal liabilities arising from this are unrelated to Tencent.
4. Without Tencent's written permission, you are not authorized to use the names or logos legally owned by Tencent, such as "Tencent." Otherwise, you may be liable for legal responsibilities.
5. This open-source code does not have the ability to directly provide services to end-users. If you need to use this code for further model training or demos, as part of your product to provide services to end-users, or for similar use, please comply with applicable laws and regulations for your product or service. Any legal liabilities arising from this are unrelated to Tencent.
6. It is prohibited to use this open-source code for activities that harm the legitimate rights and interests of others (including but not limited to fraud, deception, infringement of others' portrait rights, reputation rights, etc.), or other behaviors that violate applicable laws and regulations or go against social ethics and good customs (including providing incorrect or false information, spreading pornographic, terrorist, and violent information, etc.). Otherwise, you may be liable for legal responsibilities.
```

LOGO: color and font suggestion: [ChatGPT](https://chat.openai.com), logo font: [Montserrat Alternates
](https://fonts.google.com/specimen/Montserrat+Alternates?preview.text=SadTalker&preview.text_type=custom&query=mont).

All the copyrights of the demo images and audio are from community users or the generation from stable diffusion. Feel free to contact us if you would like use to remove them.


<!-- Spelling fixed on Tuesday, September 12, 2023 by @fakerybakery (https://github.com/fakerybakery). These changes are licensed under the Apache 2.0 license. -->
