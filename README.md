# Trustworthy detection of social isolation in the elderly from multi-sensor daily activity sequences
Bardh Prenkaj, Dario Aragona, Alessandro Flaborea, Fabio Galasso, Saverio Gravina, Luca Podo, EmiliaReda, Paola Velardi

##Implementation details
For the autoencoder baselines, we set the number of epochs to 30, the batch size to 32, and the learning rate to 10^-3. 
For TadGAN, we set the epochs to 50, the batch size to 64, the learning rate to 5x10^-4 and the iteration for the critic to 5. We use Adam as the optimisation function to train all the baselines. We took inspiration from an online available PyTorch implementation at [GitHub Pages](https://github.com/arunppsg/TadGAN).
