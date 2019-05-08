### RNN_model.py
Class RNN:  classifier for sentiment analysis. Input is fixed length float vector representing a truncated sentence

### amz_loader.py
Class DatasetAmazon: customized dataset class inheriting from torch dataset module, reading multiple files stored in a single h5py dataset as input. __ getitem__ method will read the next file of input once the current file is exhausted.

### combine_h5.py: 
Execute this file to combine several h5py file into a single h5py file. Key is file name. Value corresponding to each key is a numpy array storing data chunk.

### dynamic_dataloader.py
undo_cumulative_sum:

get_batch_data_split

get_dynamic_loader

### dynamic_rnn.py
+ metric classes: Average, F1_score, and Accuracy:
+ train: perform 1 epoch of forward and backward action
+ get_dataloader:create dataset object, randomly split into 90% training data and 10% test data.

### install_boto3_h5py.sh
This file is used to perform bootstrap action in AWS EMR and install software

### mapper.py
This file is used to remove stop words, punctuations from raw text and transform text to lower case.

### reducer.py
This file is used to change words to their respective index according to a pre-loaded dictionary, truncate or pad each sentence to make it a pre-specified fixed length(100), remove duplicate and keep the mode of ratings and map ratings to binary sentiment indicator.

### sequential_rnn.py
Our code baseline. This is in general similar to dynamic_rnn.py.