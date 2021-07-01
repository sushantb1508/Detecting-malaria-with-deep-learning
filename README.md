# Detecting-malaria-with-deep-learning
This repository contains the Jupyter Notebooks to train custom CNNs and extract features from the underlying data using pretrained models applied to the challenge of Malaria Cell classification

Malaria is a blood disease caused by the Plasmodium parasites transmitted through the bite of female Anopheles mosquito. Microscopists commonly examine thick and thin blood smears to diagnose disease and compute parasitemia. However, their accuracy depends on smear quality and expertise in classifying and counting parasitized and uninfected cells. Such an examination could be arduous for large-scale diagnoses resulting in poor quality. State-of-the-art image-analysis based computer-aided diagnosis methods using machine learning techniques, applied to microscopic images of the smears using hand-engineered features demand expertise in analyzing morphological, textural, and positional variations of the region of interest. In contrast, Convolutional Neural Networks, a class of deep learning models promise highly scalable and superior results with end-to-end feature extraction and classification. Automated malaria screening using deep learning techniques could, therefore, serve as an effective diagnostic aid. In this study, we evaluate the performance of pre-trained models as feature extractors toward classifying parasitized and uninfected cells to aid in improved disease screening. We experimentally determine the optimal model layers for feature extraction from the underlying data. Statistical validation of the results demonstrates the use of pre-trained convolutional neural networks as a promising tool for feature extraction for this purpose.

# Microscopic Diagnosis

Malaria parasites can be identified by examining under the microscope a drop of the patient’s blood, spread out as a “blood smear” on a microscope slide. Prior to examination, the specimen is stained to give the parasites a distinctive appearance. This technique remains the gold standard for laboratory confirmation of malaria. However, it depends on the quality of the reagents, of the microscope, and on the experience of the laboratorian.WHO recommends that all cases of suspected malaria be confirmed using parasite-based diagnostic testing (either microscopy or rapid diagnostic test) before administering treatment. Results of parasitological confirmation can be available in 30 minutes or less.

![59105133-e5f5f000-8950-11e9-9a09-b0b782a8305b](https://user-images.githubusercontent.com/64475805/124130905-e2d07e00-da9c-11eb-980f-068a1a82837e.jpg)

# Transfer Learning Model To detect malaria

This project uses a Deep Neural Network, more specifically a Convolutional Neural Network, to differentiate between microscopic images and determine whether person is having malaria or not.I have used the concept of Transfer learning which required pre-trained model so, in this project I have used MobileNet convolutional neural network.In this pre-trained model does not contain our images so we have to provide our own images to predict infected person .The CNN manages to get an accuracy of 98% on the training set and 92% on the test set after that we eill save the model and Then stored weights of this CNN Model are used to classify Malaria parasites.

# Malaria model training summary

![accuracy](https://user-images.githubusercontent.com/64475805/124134059-119c2380-daa0-11eb-8aad-d949dadccc98.jpg)

# Optimal Learning Rate

The learning rate is the most important hyper-parameter for training neural networks, yet until recently deciding its value has been incredibly shady.. We do a trial run and train the neural network using a low learning rate, but increase it exponentially with each batch Meanwhile, the loss is recorded for every value of the learning rate. We then plot loss against learning rate .The optimum learning rate is determined by finding the value where the learning rate is highest and the loss is still descending.

![train and test loss](https://user-images.githubusercontent.com/64475805/124134447-78214180-daa0-11eb-9c47-ec3382b92878.jpg)

# Deployment Of The Model

Creating Machine Learning models is nowadays becoming increasingly easy thanks to many open-source and proprietary based services (e.g. Python, R, SAS). Although, practitioners might always find it difficult to efficiently create interfaces to test and share their completed model to colleagues or stakeholders.
One possible solution to this problem is Gradio, a free open-source Python package which helps you to create models user interfaces which you can effortlessly share with a link to colleagues and friends.

PERSON IS NOT INFECTED BY MALARIA

![gradio1](https://user-images.githubusercontent.com/64475805/124136132-1bbf2180-daa2-11eb-941d-96d3990a1b4d.jpg)

PERSON IS INFECTED BY MALARIA

![gradio2](https://user-images.githubusercontent.com/64475805/124136617-8ff9c500-daa2-11eb-98b9-c05b72355af3.jpg)







