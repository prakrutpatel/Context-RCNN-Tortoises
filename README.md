# Context R-CNN Training

Context R-CNN is an object detection algorithm that uses contextual features to improve object detection. It is based on Faster R-CNN, but it adds a module that can incorporate contextual features from surrounding frames. This allows Context R-CNN to better identify objects that are partially obscured or that are moving quickly.

The contextual features are stored in a memory bank, which is built up over time as the camera captures images. The memory bank is indexed using an attention mechanism, which allows Context R-CNN to focus on the most relevant contextual features for each object.

Context R-CNN has been shown to improve object detection performance on a variety of datasets, including camera trap data and traffic camera data. It is a promising approach for improving object detection in static monitoring cameras, where the sampling rate is low and the objects may exhibit long-term behavior.

 Context R-CNN was developed by some very smart people but I'm not one of them. I do hope to reach that level some day :)
 
 If you're interested in reading the research paper, it can found [here](https://arxiv.org/abs/1912.03538).
This repo simply demostrates how to build you own Context RCNN model using a custom dataset. If you're interested in testing out the results, visit this [Hugging Face](https://huggingface.co/spaces/prakrutpatel/ContextRCNN_Gradio) page that shows the result from my Gopher Tortoises dataset.

## Training Steps
#### Each notebook contains intructions that you can follow
- Create a Faster R-CNN model using your custom dataset. File - [Faster RCNN Training.ipynb](https://github.com/prakrutpatel/Context-RCNN-Tortoises/blob/main/Faster%20RCNN%20Training.ipynb)
- Add Embedding and Context to your tfrecords. File - [Embedding Context Maker.ipynb](https://github.com/prakrutpatel/Context-RCNN-Tortoises/blob/main/Embedding%20Context%20Maker.ipynb)
- Create a Context R-CNN model using your custom dataset. File -[Context RCNN Training.ipynb](https://github.com/prakrutpatel/Context-RCNN-Tortoises/blob/main/Context%20RCNN%20Training.ipynb)

Upon completing training both Faster and Context R-CNN models. You can use [Faster R-CNN vs Context R-CNN.ipynb](https://github.com/prakrutpatel/Context-RCNN-Tortoises/blob/main/Faster%20R-CNN%20vs%20Context%20R-CNN.ipynb) to compare both models. This notebook contains foundational steps to implementing the models into a system.

> Supporting config files used by me during the training are located in Examples folder
