# csgy6613-project

Project work for CS-GY-6613 Spring 2024: Artificial Intelligence

David Hauss: dh3382

Andres Zarta: aza219

## Milestone 1 Submission
All relevant files are in the [ML1 folder](ML1). See [test_samgeo.ipynb](ML1/test_samgeo.ipynb) for successful PyTorch and Samgeo test and [load_data.ipynb](ML1/load_data.ipynb) for the data streaming setup. [QGIS-screenshot.png](ML1/QGIS-screenshot.png) shows QGIS running locally after succcessful installation, [running_container.png](ML1/running_container.png) shows the container running locally, and the .tif and .gpkg files are output from running [test_samgeo.ipynb](ML1/test_samgeo.ipynb). The notebooks will run smoothly using the repo's dockerfile and dev container folder on any Ubuntu system with an Nvidia GPU that has the [Nvidia container toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html) installed. Note that the original [requirements.in](requirements/requirements.in) has been modified by downgrading the OpenCV version to 4.8.0.74 in order to avoid a dependency issue with samgeo, and also by adding huggingface hub to the requirements.

## Milestone 2 Submissions
All relevant files are in the [ML2 Folder](ML2). Cell ouput from the [AutoMaskGenerator](ML2/AutoMaskGenerator.ipynb) notebook demonstrates that the [samgeo tutorial](https://www.youtube.com/watch?v=YHA_-QMB8_U&embeds_referring_euri=https%3A%2F%2Fpantelis.github.io%2F&source_ve_path=MjM4NTE&feature=emb_title) was successfully implemented in our environment.

## Milestone 3
All relevant files are in the [ML3 Folder](ML3). The [finetune.ipynb](ML3/finetune.ipynb) notebook was used for training and initial testing of our models, and the [model_testing.ipynb](ML3/model_testing.ipynb) notebook includes further testing of the two models we trained. Using Colab's A100 Nvidia setup with High RAM, we trained on a subset of the given dataset for 4 Epochs, which took 2 hours -> ~0.51 final loss. Training on the full dataset set for 2 Epochs took 7 hours with a ~0.50 final loss rate. We found great performance from both models by testing on the val set, but opted for the model trained on the full dataset due to the fact that it would likely have more generalizable results.
