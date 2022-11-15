# ActRecogConvLSTM_LRCN
Jupyter Notebook implementation of Human Activity Recognition using ConvLSTM and Long-term Recurrent Convolutional Networks (LRCN)

## Dataset Used
The dataset used in the training process is the UCF50 - Action Recognition Data Set. Dataset can be downloaded from [this link](https://www.crcv.ucf.edu/data/UCF50.php)</br>
The dataset contains:
- 50 Action Categories
- 25 Groups of Videos per Action Category
- 133 Average Videos per Action Category
- 199 Average Number of Frames per Video
- 320 Average Frames Width per Video
- 240 Average Frames Height per Video
- 26 Average Frames Per Seconds per Video


## PreProcessing
- `Sequence length = 20` has been selected to be feeded into both the networks (ConvLSTM, LRCN). <\br>
- `Image_width, Image_height = 64, 64` set for the input sequences/frames to be feeded into the networks
- `Training Data = 60%`, `Validation Data = 20%`, `Testing Data = 20%` has been set.

## ConvLSTM Model Architecture
The ConvLSTM model architecture is described below: </br>
![ConvLSTM Model Architecture](https://github.com/Erfan-Mostafiz/ActRecogConvLSTM_LRCN/blob/main/Illustrations/convLSTM_model_architecture.png)

## Long-term Recurrent Convolutional Network (LRCN) Model Architecture
The LRCN model architecture is described below:</br>
![LRCN Model Architecture](https://github.com/Erfan-Mostafiz/ActRecogConvLSTM_LRCN/blob/main/Illustrations/LRCN_model_architecture.png)
</br>

## ConvLSTM Model Performance
After training on `20 epochs` early stopping CallBack was triggered. `Test Accuracy = 70%`, and `Test Loss = 70%` </br>
![ConvLSTM model accuracy](https://github.com/Erfan-Mostafiz/ActRecogConvLSTM_LRCN/blob/main/Illustrations/ConvLSTM%20Accuracy.png)
![ConvLSTM model loss](https://github.com/Erfan-Mostafiz/ActRecogConvLSTM_LRCN/blob/main/Illustrations/ConvLSTM%20loss.png)

## LRCN Model Performance
After training on `37 epochs` early stopping CallBack was triggered. `Test Accuracy = 86%`, and `Test Loss = 55%` </br>
![LRCN model accuracy](https://github.com/Erfan-Mostafiz/ActRecogConvLSTM_LRCN/blob/main/Illustrations/LRCN%20Accuracy.png)
![LRCN model loss](https://github.com/Erfan-Mostafiz/ActRecogConvLSTM_LRCN/blob/main/Illustrations/LRCN%20Loss.png)

The Long-term Recurrent Convolutional Network (LRCN) had a better training and testing accuracy and less loss, and the training time was comparitively faster than the ConvLSTM model network.

 - The best weights are stored in `Models` folder
 - The Training Logs are stored in `Training Logs` folder
