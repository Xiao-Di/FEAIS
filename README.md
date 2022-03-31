# FEAIS

**A Facial Emotion Recognition Enabled Education Aids IoT System for Online Learning**

The source code for the [IEEE ICALT2022](https://tc.computer.org/tclt/icalt-2022/) conference paper, which proposes a Facial Emotion Recognition (FER) Enabled Education Aids IoT System, named FEAIS. By deploying a well-trained FER model on the remote server, FEAIS can provide instant feedback on students’ learning state by collecting their facial pictures through IoT devices like cameras or vision sensors and making recognization on their emotion. Utilizing this information, teachers can adjust their teaching progress to ensure that everyone could catch up.

### Architecture

[System architecture](./network.pdf)

The proposed FEAIS is composed of Three parts, i.e. **Pre-processing module**, **In-built FER model** and **Score-calculating module**.

* *Pre-processing module*

    * Face detection
    * Facial normalization

* *In-built FER model*

    A pre-trained FER model based on CNN architecture is trained and then deployed on the remote server.

    * Data augementation

    * FER model architecture

        An **EfficientNet network** is used as a feature extractor after augmenting the re-classified *FER2013+* dataset.

        * EfficientNet Feature Extractor
        * Classifier

* *Score-calculating module*

### Dataset

The in-built FER model is trained on the benchmark dataset, named **FER2013+**, which consists of thousands of 48×48 pixel grayscale images of faces collected from Google search engine.

There are a total number of 25,060 images in the training set and 3199 images in the validation set, comprising eight categories of happy, contempt, fear, surprise, sadness, neutral, anger and disgust.

However, the main purpose of this paper is to help teachers have a better understanding of students’ learning state, detailed classification is not necessary. So we combine contempt, fear, surprise, sadness, anger, and disgust into a new category and therefore adjust the dataset to a triple-classification one to make it more suitable for the online learning case.



### Results


