# KnowZRel: Common Sense Knowledge-based Zero-Shot Relationship Retrieval for Generalized SGG

[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/knowzrel-common-sense-knowledge-based-zero/scene-graph-generation-on-visual-genome)](https://paperswithcode.com/sota/scene-graph-generation-on-visual-genome?p=knowzrel-common-sense-knowledge-based-zero)
[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/knowzrel-common-sense-knowledge-based-zero/scene-graph-generation-on-gqa)](https://paperswithcode.com/sota/scene-graph-generation-on-gqa?p=knowzrel-common-sense-knowledge-based-zero)

This readme file provides an overview of the codebase for the paper implementation. The download links and destination paths for the dataset, Faster RCNN model and CSKG embeddings are provided. The notebooks [ZS_SGG_FasterRCNN/ZS_SGG_FasterRCNN.ipynb](ZS_SGG_FasterRCNN/ZS_SGG_FasterRCNN.ipynb) and [ZS_SGG_CSKG/j_SG_CSKG_ZeroShot.ipynb](ZS_SGG_CSKG/j_SG_CSKG_ZeroShot.ipynb) can be used to reproduce the results. A thoroughly documented codebase/toolkit with examples/demo of the proposed method will be released soon.

![Block Diagram](https://github.com/jaleedkhan/zsrr-sgg/assets/71158275/61d6fac4-3683-46a6-b1b6-01c433203d5f)

## Requirements
- Ubuntu 18.04
- CUDA 10.1
- Python 3.7
- PyTorch 1.4
- KGTK 0.5

## Code:
- Object detection: ZS_SGG_FasterRCNN/ZS_SGG_FasterRCNN.ipynb
- Zero-shot relationship retrieval and zero-shot SGG evaluation: ZS_SGG_CSKG/j_SG_CSKG_ZeroShot.ipynb

## Directories:
- [ZS_SGG_FasterRCNN](ZS_SGG_FasterRCNN) contains code, data and model for object detection.
- [ZS_SGG_CSKG](ZS_SGG_CSKG) contains code, data and CSKG embeddings for zero-shot relationship retrieval for scene graph generation
- [Eval_IO](Eval_IO) contains input/output data files for evaluation
- [Eval_IO/0_images](Eval_IO/0_images) contains Visual Genome images.
- [Eval_IO/1_det_objs](Eval_IO/1_det_objs) contains detected objects info.
- [Eval_IO/2_zs_sg](Eval_IO/2_zs_sg) contains generated scene graphs with zero-shot relationships extracted from CSKG.

## Downloads and destination paths:
### Datasets
- Visual Genome: Download [images.zip](https://cs.stanford.edu/people/rak248/VG_100K_2/images.zip) and
  [images2.zip](https://cs.stanford.edu/people/rak248/VG_100K_2/images2.zip) and unzip all images to Eval_IO/0_images. Also download [relationships.json](https://visualgenome.org/static/data/dataset/relationships.json.zip) and [image_data.json](  https://visualgenome.org/static/data/dataset/image_data.json.zip) and place both files in the root directory.
- GQA: [https://cs.stanford.edu/people/dorarad/gqa/download.html](https://cs.stanford.edu/people/dorarad/gqa/download.html)
### CSKG Embeddings:
- Download all files from [this link](https://drive.google.com/drive/u/1/folders/16347KHSloJJZIbgC9V5gH7_pRx0CzjPQ) and 
  place them in ZS_SGG_CSKG/cskg/output directory.
- Move 'bert_nli_large_w2v_format.txt.gz' to ZS_SGG_CSKG/cskg/output/embeddings directory.
- Download [numberbatch file](https://conceptnet.s3.amazonaws.com/downloads/2019/numberbatch/numberbatch-19.08.txt.gz) and place
  it in ZS_SGG_CSKG/cskg/output/embeddings directory.
### Pre-trained Faster RCNN model:
- Download [model1](https://1drv.ms/u/s!AmRLLNf6bzcir8xemVHbqPBrvjjtQg?e=hAhYCw) and [model2](https://1drv.ms/u/s!AmRLLNf6bzcir9x7OYb6sKBlzoXuYA?e=s3Y602), and place them in 'ZS_SGG_FasterRCNN/'.
