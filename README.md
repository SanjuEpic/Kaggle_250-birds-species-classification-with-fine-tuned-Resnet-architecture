# Kaggle_250-birds-species-classification-with-fine-tuned-Resnet-architecture

The dataset was taken from kaggle which consisted of 250 different bird species.(size of ~1.5-2GB)
Due to the heavy size I have used the kaggle API to launch the dataset directly from Google Colab notebook(doing on kaggle itself is also an option!)
We have even setup a benchmark model (a basic CNN model) for comparing the results with the later built Resnet architecture

The dataset consists of 37k images in total belonging to 250 different species of birds.

## Keras tuner
You can find the link for the documentation of keras tuner here: https://keras-team.github.io/keras-tuner/

We have fine tuned the hyperparameters of the Resnet architecture for finding the best set of hyperparameters and achieved an accuracy of around 95% on validation dataset
(which was trained for over 3 days/140 epochs)

## TFlite model

### The Process
![TF](https://user-images.githubusercontent.com/57587354/108491006-639a9480-72c9-11eb-95bd-48e9ec099631.jpg)




At last after the model was trained, the saved model was then converted into tflite(Tensorflow lite for small devices)model,
so that it could be deployed onto the android version of mobile for using the real-time object detection of these bird species.



Link for further deployment help can be taken from here: https://developers.google.com/ml-kit/vision/object-detection/custom-models/android
