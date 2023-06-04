# Socratic Models for Image Captioning and Multimodal Reasoning

## Overview
 Socratic models (SMs) [[1]](#1) is a modular framework in which multiple pre-trained models are composed zeroshot via multimodal informed prompting. This is done to exchange information between models and capture new multimodal capabilities, without requiring finetuning. As a proof of concept, we modify the Socratic models framework such that it is entirely open-source and attempt to achieve the same results as the original version. Additionally, we investigate the capabilities of Socratic models on multimodal reasoning tasks such as chain-of-thought reasoning and visual question-answering in zeroshot and few-shot settings.

## Code
### Installation
To install the environment, run:

`conda env create -f environment.yml`  
`conda activate socratic`  
`python -m spacy download en`

### Instructions
This repository provides scripts for CLIP with GPT-3, FLAN-T5, GitVision, BLIP and BLIP2 prompting, and self-contained ipython notebooks with prototype implementations of Socratic Models for image captioning geenration, chain-of-thought and visual question answering.The project was organised such that the downloading, caching and organisation of files is managed by the code. The classes were built in a modular fashion such that they could be adapted to different use-cases.

### Notes on files in this repository

* **scripts**
  * `coco_caption_base.py` - Run a train/valid/test dataset on the Baseline Image Captioner.
  * `coco_caption_base_hp_tune.py` - Run a parameter search on the Baseline Image Captioner.
  * `coco_caption_imp.py` - Run a train/valid/test dataset on the Improved Image Captioner.
  * `coco_caption_imp_hp_tune.py` - Run a parameter search on the Improved Image Captioner.
  * `coco_caption_gpt.py` - Run a train/valid/test dataset on the Original Socratic Captioner.
  * `coco_caption_git.py` - Run a train/valid/test dataset using GIT.
  * `coco_caption_blip.py` - Run a train/valid/test dataset using BLIP.
  * `coco_caption_blip2.py` - Run a train/valid/test dataset using BLIP2.
  * `image_captioning.py` - Contains the functionality relating to the image captioning.
  * `mm_reasoning.py` - Contains the functionality relating to the multimodal reasoning.
  * `generate_reasoning.py` - Run a reasoning task.
  * `utils.py` - Contains utilities functions.
  * `coco_evaluation.py` - Run the evalutaion of the captions that were generated using different approaches.
  * `reasoning_evaluation.py` - Run the multimodal reasoning evalutation.

* **notebooks**
    * `demo_baseline.ipynb` - A demo of the Baseline Image Captioner in action.
    * `demo_improved.ipynb` - A demo of the Improved Image Captioner in action.
    * `demo_gpt.ipynb` - A demo of the Original Socratic Image Captioner in action.
    * `demo_gitvision.ipynb` - A demo of GIT in action.
    * `demo_blip.ipynb` - A demo of BLIP in action.
    * `demo_blip2.ipynb` - A demo of BLIP2 in action.
    * `display_images_captions.ipynb` - A display of a selection of captions that were obtained with the captioners.
    * `visualise_CLIP.ipynb` - Visualisations of the embedding space of CLIP.
    * `socratic_mm_reasoning.ipynb` - A showcase of the multimodal reasoning tasks.

* **data**
  * The data directory stores the input and generated data. It is automatically created when the code is run.


## References
<a id="1">[1]</a> Zeng, A. et al. Socratic models: Composing zero-shot multimodal reasoning with language. arXiv
preprint arXiv:2204.00598 (2022).

## License
This project is licensed under the terms of the [MIT License](https://opensource.org/licenses/MIT), allowing free use of the code.

