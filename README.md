# Image Captioning PyTorch

### An overview

The project presents an Image Captioning model pretrained on ImageNet to generate captions for the Flickr8k dataset. A convolutional neural network (CNN) has been used to conduct feature extraction on Flikr8k images. Those feature vectors are then passed to a recurrent neural network (RNN). We used a long short-term memory (LSTM) RNN because the feedback connections allow us to process sequences of data. The target captions are fed into the RNN and converted to vector embeddings. These are combined with the image vectors before being processed by the LSTM layer. To generate captions, we feed each LSTM cell output into another LSTM cell to produce a sequence of words that are combined to create a caption.

We've conducted two experiments - ResNet50 and ResNeXt50 as pretrained feature extractors. Both of them seem to provide different results. While ResNeXt50 outperforms ResNet50 in classification tasks, in this case, the ResNet model seems to perform better.

### Implementation Details

To run the training script, please run:

```{bash}
python3 train.py
```

To download the dataset, please visit:
https://www.kaggle.com/datasets/adityajn105/flickr8k
