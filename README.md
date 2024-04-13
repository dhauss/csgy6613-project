# csgy6613-project

Project work for CS-GY-6613 Spring 2024: Artificial Intelligence

David Hauss: dh3382

Andres Zarta: aza219

## Milestone 1 Submission
All relevant files are in the [ML1 folder](ML1). See [test_samgeo.ipynb](ML1/test_samgeo.ipynb) for successful PyTorch and Samgeo test and [load_data.ipynb](ML1/load_data.ipynb) for the data streaming setup. [QGIS-screenshot.png](ML1/QGIS-screenshot.png) shows QGIS running locally after succcessful installation, [running_container.png](ML1/running_container.png) shows the container running locally, and the .tif and .gpkg files are output from running [test_samgeo.ipynb](ML1/test_samgeo.ipynb). The notebooks will run smoothly using the repo's dockerfile and dev container folder on any Ubuntu system with an Nvidia GPU that has the [Nvidia container toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html) installed. Note that the original dockerfile has been modified by downgrading the openCV version to avoid a dependency issue with samgeo, and also by adding huggingface hub to the requirements.
