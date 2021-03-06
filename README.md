# smARtgestures
In this repo you can find the code I wrote for my bachelor thesis. The thesis analysed convolutional neural networks for recognizing hand gestures which were performed on the Microsoft HoloLens. A more detailed explaination can be found on [kaggle](https://www.kaggle.com/tobirohrer/hololens-gesture-data).

```
smARtgesetures
│   README.md  
│
└───application
│   └───networks
│       │   Executable NNs as jupyter notebooks
│   └───scripts
│       │   Scripts for data augmentation and preprocessing. 
└───gestureData
│   │    Trainings and testdata of the 4 different gestures.
└───gestureDataExtractor
│   │    Scripts written in c# to extract gesture data using unity.
```

## Gesture data
In the beginning, there was no gesture data which could be used for this work. Therefore, 600 real gesture data from four different classes where created in real interaction with the Microsoft HoloLens. Data augmentation was applied to increase the data used for training and evaluating the network.

To do so, a Unity szene plus scripts for extracting gesture data from hand movements was created.

## Network
The CNNs were implemented using TensorFlow.

## Results
The implemented two dimensional convolutional network achieved a classification accuracy of 100% on the test data (200 of the 600 real data) and 95,68% on gestures which were done by other persons (foreign gestures). The implemented three dimensional convolutional network was able to achieve a classification accuracy of 99% on the test data and 91,35% on the foreign gestures. In an experiment, the three dimensional implementation was trained by only 10% of the training data and achieved a classification accuracy of 92% and on the test data and 86,49% on the foreign gestures. Visualizations of the parameters, which were learned by the network could show gesture properties which were detected by the network. In a further experiment, the implemented three dimensional network was analyzed using data which was extended by time information. In this experiment the network archived a classification accuracy of 99,25% on the test data and 89,19% on the foreign gestures.
