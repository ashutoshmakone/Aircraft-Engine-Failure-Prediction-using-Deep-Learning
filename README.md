# Aircraft-Engine-Failure-Prediction-using-Deep-Learning
Classification Case Study for Aircraft Engine Failure

### The Dataset provided by NASA contains three types of files
1. train_FD001.txt (Training data) -->  It is the aircraft engine run-to-failure data.
2. test_FD001.txt(Testing data) --> It is the aircraft engine operating data without failure events recorded.
3. RUL_FD001.txt(Ground truth data) --> It contains the information of true remaining cycles for each engine in the testing data.

### Task
The task is to predict whether a given Aircraft Engine will fail within next 30 cycles or not

### Feature Information:
1. unit_id has values from 1 to hundred. These values correspond to 100 engines
2. Number of cycles over of engine is given by 'cycles'
3. The last cycle for a unit_id is where that engine failed
4. set1,set2,set3 are three different setting of engines
5. s1 to s23 are sensor data of 23 sensors

### Modeling
Remaining useful life of train data is not provided. So it is generated using given information.
Keras sequencial model with two LSTM layers and adam optimizer is used. L2 regularization is used.
A recall of 0.9082 is obtained
