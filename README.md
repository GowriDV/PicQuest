# PicQuest: Hybrid Search Mechanism
A hybrid search system that includes both object and text recognition to incorporate flexibility in the search process. It includes a caption generation model for object recognition and an optical character recognition model for text recognition. Traditional search mechanisms involved keyword matching. Object recognition using deep learning introduced a better technique for searching. I have attempted to combine object and text recognition both to create a hybrid search mechanism. 
## Model Architecture
### Image Caption Generation
This model generate appropriate caption describing the visuals in the image. 
#### 1. Data preprocessing :
Resizing and preprocessing it as required for the feature extractor using preprocess_input.
The captions are loaded and all non-alpha characters are omitted. The characters are then converted to lowercase and 'start' and 'end' tags are added to the beginning and end of the caption.
#### 2. Model training :
Model is trained on about 8000 images from Flickr8k dataset. It is then passed through encoder decoder model.
### OCR 
This model detects and recognises text present in images.
#### 1. Data preprocessing :
Resizing and normalising the images.
Legible and English annotations are filtered out.
Augmentations are als carried out
#### 2. Model training :
Model is trained on COCO-Text 2017 dataset. It is then passed through a CRNN model with bidirectional LSTM.
### Final Pipeline
In final pipeline involves:
1. Generating captions for images in the dataset.
2. Detects and labels any text present in the image.
3. Matching with text prompt using cosine similarity.
###  Final Deliverable
The most relevant image related to the text prompt is displayed. The primary output of my project is a functional, integrated search system that combines object recognition, text recognition, and flexible search capabilities. This reduces dependency on keyword based searching and implements a hybrid approach.
### TECH STACK
## Programming Language
- **Python**
## Libraries
- **TensorFlow**
- **Keras** - High-level neural networks API running on top of TensorFlow
- **MatplotLib** 
- **Numpy**
- **tqdm**
- **pickle**
- **json**
- **torch**
### Environment
Google Colab
