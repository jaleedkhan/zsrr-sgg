--------------------------------------------------------------------------------------------------------------
Welcome!
--------------------------------------------------------------------------------------------------------------
This readme file provides an overview of the codebase for the paper implementation. The sizes of the dataset, 
Faster RCNN model and CSKG embeddings are too large and are not included in the files. However, the download 
links and locations to place them are provided. The code notebooks ZS_SGG_FasterRCNN/ZS_SGG_FasterRCNN.ipynb
and ZS_SGG_CSKG/j_SG_CSKG_ZeroShot.ipynb can be used to reproduce the results. A thoroughly documented 
codebase/toolkit with examples/demo of the proposed method will be released open source on GitHub with the 
camera ready paper.

--------------------------------------------------------------------------------------------------------------
Code Notebooks/Files and Directories:
--------------------------------------------------------------------------------------------------------------
- 'ZS_SGG_FasterRCNN/ZS_SGG_FasterRCNN.ipynb' (Code for object detection)
- 'ZS_SGG_CSKG/j_SG_CSKG_ZeroShot.ipynb' (Code for zero-shot relationship retrieval and zero-shot SGG 
   evaluation)
- 'ZS_SGG_FasterRCNN' (contains code/data/model of object detection)
- 'ZS_SGG_CSKG' (contains code/data/model of CommonSense Knowledge Graph (CSKG) and zero-shot relationship
   retrieval for scene graph generation)
- 'Eval_IO' (contains input/output data files for evaluation)
- 'Eval_IO/0_images' (contains Visual Genome images)
- 'Eval_IO/1_det_objs' (contains detected objects info)
- 'Eval_IO/2_zs_sg' (contains generated scene graphs with zero-shot relationships extracted from CSKG)

--------------------------------------------------------------------------------------------------------------
Downloads:
--------------------------------------------------------------------------------------------------------------
Visual Genome Dataset:
- Download https://cs.stanford.edu/people/rak248/VG_100K_2/images.zip and
  https://cs.stanford.edu/people/rak248/VG_100K_2/images2.zip and unzip all images to 'Eval_IO/0_images'
- Download https://visualgenome.org/static/data/dataset/relationships.json.zip and 
  https://visualgenome.org/static/data/dataset/image_data.json.zip and place both files in root directory.
CSKG Embeddings:
- Download all files from https://drive.google.com/drive/u/1/folders/16347KHSloJJZIbgC9V5gH7_pRx0CzjPQ and 
  place them in 'ZS_SGG_CSKG/cskg/output' directory. 
- Move 'bert_nli_large_w2v_format.txt.gz' to 'ZS_SGG_CSKG/cskg/output/embeddings' directory. 
- Download https://conceptnet.s3.amazonaws.com/downloads/2019/numberbatch/numberbatch-19.08.txt.gz and place
  it in 'ZS_SGG_CSKG/cskg/output/embeddings' directory.
Pre-trained Faster RCNN:
- Download https://1drv.ms/u/s!AmRLLNf6bzcir8xemVHbqPBrvjjtQg?e=hAhYCw and 
  https://1drv.ms/u/s!AmRLLNf6bzcir9x7OYb6sKBlzoXuYA?e=s3Y602 and place them in 'ZS_SGG_FasterRCNN/'