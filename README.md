# Spotify Song Clustering

Nicolas Thiel (i6254307)

MSB1015 Scientific Programming

Maastricht University

This project is part of the assessments for the course MSB1015 Scientific Programming.

## Requirements
Required packages are defined in requirements.txt and can be installed using `pip install requirements.txt`

The original data can be dowloaded from [Kaggle](https://www.kaggle.com/datasets/zaheenhamidani/ultimate-spotify-tracks-db/data). The data (original, adjusted, and cleaned) can be downloaded from [this drive](https://drive.google.com/drive/folders/1osmTrrS8K6LbhdcZH6vr91OW8md-1jbr?usp=sharing). An explanation of each feature can be found [here](https://developer.spotify.com/documentation/web-api/reference/get-audio-features).

## Description
In this project songs that were queried from Spotify DB are clustered. The goal is to define clusters of similar songs that are not connected to the genre of the song. The code provided in this repository allows the user to reprodce the results and figures shown in the final presentation.

In `data_cleaning.ipynb` the original data is loaded, inspected, and cleaned. Finally, outlier detection using Isolation Forest is carried out.

In `clustering.ipynb` the cleaned data is used to infer clusters using (1) k-means on the scaled data, (2) k-means on pca-reduced data, (3) agglomerative clustering on a distance matrix derived by an unsupervised random forest, and (4) k-prototypes on scaled and encoded data.
