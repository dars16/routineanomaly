# Trustworthy detection of social isolation in the elderly from multi-sensor daily activity sequences
Bardh Prenkaj, Dario Aragona, Alessandro Flaborea, Fabio Galasso, Saverio Gravina, Luca Podo, EmiliaReda, Paola Velardi

## Implementation details
For the autoencoder baselines, we set the number of epochs to 30, the batch size to 32, and the learning rate to 10^-3. 
For TadGAN, we set the epochs to 50, the batch size to 64, the learning rate to 5x10^-4 and the iteration for the critic to 5. We use Adam as the optimisation function to train all the baselines. We took inspiration from an online available PyTorch implementation at [TadGAN](https://github.com/arunppsg/TadGAN).

## Datasets
In Datasets folder are stored the 3 datasets used as benchmark, each of them represented by the following files:
- normal_sequences.pt : [Num_sequences, Window_size = 30, N_features = 5]
- activity_codes.json : dictionary containing the mapping between numerical labels and activities.
- POINT_ANOMALIES : folder containing four anomalous test sequences, identified by their name and provided in the format specified for normal_sequences.pt, associated with the groundtruth.

The features are described as follows:

0. label : numerical label representing the action carried on (see activity_code.json for the conversion to human-readable format).
1. beginTS : normalised numerical value representing the timestamp of the day the action is carried on [0, 1].
2. duration : duration of an action normalised in [0,1] w.r.t to all the durations of the same activity type.
3. dayPart : to account for the temporal collocation of the activity in a particular day, we divide it in four daily slots corresponding to night, morning, afternoon, and evening, mapped as [0,1,2,3].
4. dayFrequency : frequency of an action occurring in a day, normalised in [0,1] w.r.t. to the frequencies of activities of the same type.
