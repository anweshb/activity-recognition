# Human Video Activity Recognition

## Aim 
## The aim of this project is to classify video sequences, each of 10 frames into one of the seven different activities mentioned below in the dataset description

## Dataset
### This dataset used was taken from [Kaggle](https://www.kaggle.com/datasets/sharjeelmazhar/human-activity-recognition-video-dataset)

| Label | Label Name                      | Total Count |
|-------|---------------------------------|-------------|
| 0     | Clapping                        | 146         |
| 1     | Meet and Split                  | 147         |
| 2     | Sitting                         | 156         |
| 3     | Standing Still                  | 174         |
| 4     | Walking                         | 171         |
| 5     | Walking While Reading Book      | 176         |
| 6     | Walking While Using Phone       | 143         |


## Model Architecture

### The model takes in a video sequence with 10 frames, with each frame being a 100x100 RGB images

### The video frames are passed through 3 Convolutional Layers which serve as spatial feature extractors.

### The extracted features are lattened and passed through a Multi-Head Attention block having 8 heads and n_k = 64 for temporal feature extraction. 

### These features are passed into 2 fully connected layers, with the second one being the output layer.


## Results

### The model achieved an overall accuracy of 98.71%, more detailed results are displayed in the table below.

|    Label    | Precision | Recall | F1-Score | Support |
|:-----------:|:---------:|:------:|:--------:|:-------:|
|      0      |   1.00    |  1.00  |   1.00   |   38    |
|      1      |   1.00    |  0.91  |   0.95   |   32    |
|      2      |   1.00    |  1.00  |   1.00   |   30    |
|      3      |   1.00    |  1.00  |   1.00   |   39    |
|      4      |   0.91    |  1.00  |   0.96   |   32    |
|      5      |   1.00    |  1.00  |   1.00   |   37    |
|      6      |   1.00    |  1.00  |   1.00   |   26    |
| **Accuracy** |   0.99    |  0.99  |   0.99   |  234    |
| **Macro Avg**|   0.99    |  0.99  |   0.99   |  234    |
|**Weighted Avg**| 0.99    |  0.99  |   0.99   |  234    |
