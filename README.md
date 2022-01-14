# Trustworthy detection of social isolation in the elderly from multi-sensor daily activity sequences
Bardh Prenkaj, Dario Aragona, Alessandro Flaborea, Fabio Galasso, Saverio Gravina, Luca Podo, EmiliaReda, Paola Velardi

## Implementation details
For the autoencoder baselines, we set the number of epochs to 30, the batch size to 32, and the learning rate to 10^-3. 
For TadGAN, we set the epochs to 50, the batch size to 64, the learning rate to 5x10^-4 and the iteration for the critic to 5. We use Adam as the optimisation function to train all the baselines. We took inspiration from an online available PyTorch implementation at [TadGAN](https://github.com/arunppsg/TadGAN).

## Datasets
In Datasets folder are stored the 3 datasets used as benchmark, each of them represented by the following files:
- normal_sequences.pt : [N_sequences, Window_size, N_features]
- activity_codes.json : dictionary containing the mapping between numerical labels and activities.
- POINT_ANOMALIES : folder containing four anomalous test sequences, identified by their name and provided in the format specified for normal_sequences.pt, associated with the groundtruth.
