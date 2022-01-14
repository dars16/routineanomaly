# Trustworthy detection of social isolation in the elderly from multi-sensor daily activity sequences
Bardh Prenkaj, Dario Aragona, Alessandro Flaborea, Fabio Galasso, Saverio Gravina, Luca Podo, EmiliaReda, Paola Velardi

##Implementation details
la prof diceva di mettere le implementation details su un github
For the autoencoder baselines, we set the number of epochs to 30, the batch size to 32, and the learning rate to $10^{-3}$. For TadGAN, we set the epochs to 50, the batch size to 64, the learning rate to $5\times10^{-4}$
%and the iteration for the critic to 5. We use Adam as the optimisation function to train all the baselines.
we took inspiration from an online available PyTorch implementation\footnote{\url{https://github.com/arunppsg/TadGAN}}.
