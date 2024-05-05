# csgy6613-project

Project work for CS-GY-6613 Spring 2024: Artificial Intelligence

David Hauss: dh3382

Andres Zarta: aza219

## Milestone 1 Submission
All relevant files are in the [ML1 folder](ML1). See [test_samgeo.ipynb](ML1/test_samgeo.ipynb) for successful PyTorch and Samgeo test and [load_data.ipynb](ML1/load_data.ipynb) for the data streaming setup. [QGIS-screenshot.png](ML1/QGIS-screenshot.png) shows QGIS running locally after succcessful installation, [running_container.png](ML1/running_container.png) shows the container running locally, and the .tif and .gpkg files are output from running [test_samgeo.ipynb](ML1/test_samgeo.ipynb). The notebooks will run smoothly using the repo's dockerfile and dev container folder on any Ubuntu system with an Nvidia GPU that has the [Nvidia container toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html) installed. Note that the original [requirements.in](requirements/requirements.in) has been modified by downgrading the OpenCV version to 4.8.0.74 in order to avoid a dependency issue with samgeo, and also by adding huggingface hub to the requirements.

## Milestone 2 Submission
All relevant files are in the [ML2 Folder](ML2). Cell ouput from the [AutoMaskGenerator](ML2/AutoMaskGenerator.ipynb) notebook demonstrates that the [samgeo tutorial](https://www.youtube.com/watch?v=YHA_-QMB8_U&embeds_referring_euri=https%3A%2F%2Fpantelis.github.io%2F&source_ve_path=MjM4NTE&feature=emb_title) was successfully implemented in our environment.

## Milestone 3 Submission
All relevant files are in the [ML3 Folder](ML3). The [finetune.ipynb](ML3/finetune.ipynb) notebook was used for training and initial testing of our models, and the [model_testing.ipynb](ML3/model_testing.ipynb) notebook includes further testing of the two models we trained. Using Colab's A100 Nvidia setup with High RAM, we trained on a subset of the given dataset for 4 Epochs, which took 2 hours -> ~0.51 final loss. Training on the full dataset set for 2 Epochs took 7 hours with a ~0.50 final loss rate. We found great performance from both models by testing on the val set, but opted for the model trained on the full dataset due to the fact that it would likely have more generalizable results and that it slightly outperformed the model trained on a smaller dataset in the IoU tests (35.8% to 34.7%).

## Milestone 4 Submission
Link to the Video Demo: https://drive.google.com/file/d/1B4vOip69ltgPgDQ0Ze93l9emyzMoc7Z2/view?usp=sharing
Link to the Hugging Face Space App: https://huggingface.co/spaces/AndresZarta/ML4

As explained in the video, the Hugging Face Space Free Tier allocates a basic vCPU hardware with 16gb of RAM. Because of this, it takes about 30 seconds to complete a detection, so if you try it manually, please expect roughly that processing time. 

## Milestone 5 Submission
All relevant files are in the [ML5 folder](ML5). We attempt to use the LangSAM model for tree detection in [visual_prompting.ipynb](ML5/visual_prompting.ipynb), but the coloration of the images seems to heavily confuse the model. In [input_prompts.ipynb](ML5/input_prompts.ipynb), we attempt to use the SamGEO API to predict masks and manually prompt the map object to detect tree objects, but the API proved difficult to work with. As a last-ditch effort, we saw some potential in using a more traditional approach in [hough_transform.ipynb](ML5/hough_transform.ipynb), but alas this also proved problematic. See the respective notebooks for further clarification and test results. 
