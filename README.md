Recommendation System Using Autoencoders

This project implements a recommendation system using a Stacked Autoencoder (SAE) built with PyTorch. Autoencoders are neural networks designed for unsupervised learning tasks, capable of capturing latent patterns in user-item interactions.
Workflow

    Dataset:
        Utilizes the MovieLens dataset (ml-1m and ml-100k) for user, movie, and rating information.
        Training and test sets are prepared by transforming data into a user-movie matrix format.

    Model Architecture:
        The SAE has an encoder-decoder structure:
            Encoder: Reduces the dimensionality of the input (user-movie ratings) through hidden layers.
            Decoder: Reconstructs the original input to predict ratings.
        Activation: Sigmoid functions are used for encoding and decoding.
        Loss: Mean Squared Error (MSE) is used to optimize reconstruction quality.

    Training:
        Online learning is performed for each user to minimize memory usage.
        Observations with non-zero ratings are prioritized to improve efficiency.
        RMSprop optimizer is used for gradient descent with regularization.

    Testing:
        The model predicts ratings for unseen data and evaluates performance using the Root Mean Square Error (RMSE).
