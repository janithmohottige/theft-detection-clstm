# Theft Detection in Supermarkets using Recurrent Convolutional Neural Networks

**Theft in supermarkets** has been a long-discussed topic which the supermarkets have been trying to address through many means such as CCTV arrays, 24-hour surveillance etc. These methods are prone to failure due to human error in surveillance and human ingenuity where thieves find creative ways to steal. In this research paper, the authors propose and test different approaches to a real-time theft detection system which uses mobile edge computing to process the input video data and send only the relevant processed data back to the cloud or centralized database. Here the first approach by the authors uses **long term Recurrent Convolutional Networks** where all layers are wrapped by **time distributed layers** and sequentially of the data is maintained. As the first approach showed that the data was not enough to train the model A pre trained model named VGG16 was used to extract features and was processed to get an output. But when compared to the first approach its accuracy was lower and was not stable as well. Therefore in the third approach the authors tried to improve the accuracy and validation accuracy of the first approach by using image preprocessing prior training the model and after trying out many techniques such as **adaptive mean thresholding, OTSU thresholding, rembg background removal** and so it was found that the best results were obtained by the **OTSU thresholding** method and thus finally it was found that the LRCN approach with OTSU thresholding yielded the best results with highest accuracy and validation accuracy. After this to show the working of a system in an EDGE server the authors used a **raspberry pi 4** model B with 4gb RAM. Therefore, the author hopes the outcome of this research will help in development of more systems using this approach to help curb theft in supermarkets

## Functions of each python files

## data_preprocess.py - Preprocessing the videos data in order to make it simple for computations

## create_momdel.py - Creating the CNN-LSTM model

## Train_network.py - Training the built network using preprocessed data

## Predition_RealTime.py - Giving realtime predictions for a camera feed

## Prediction_code.py - Giving predictions using videos in local commputer

## tf_to_tflite.py - Converting saved Tensorflow model to Tensorflow Lite model in order to make it possible to run on Raspberry Pi
