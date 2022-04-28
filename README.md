# Data Project using Spotipy music features: Overview:
* Used Spotipy to access the Spotify song library via its Web API
* Sourced Spotify audio feature data to create a dataset
* Preprocessed dataset by feature selection and scaling 
* Applied clustering and dimensionality reduction techniques to data

## Objectives
1. Create clustering models and apply them to the audio features metadata
2. Investigate the feature patterns of each cluster which would characterise a music genre/style for the songs clustered

## Retrieving Data and Creating the Dataset
Spotipy, a lightweight Spotify library was used to access and retrieve the song data which consisted of 300 songs from 3 playlists (100 songs each) each representing different music styles. The data is compiled in a Pandas dataframe and exported as a csv file

## Data Preprocessing
The data is filtered down to features of continuous values and scaled. The features being worked with are Danceability, Instrumentalness, Acousticness, Energy, Liveness, Loudness, Speechiness, Tempo and Valence.

## Principal Component Analysis
The features are reduced to 4 principal components, of which the first two are used for visualisation. The total explained variance ratio is 71% (good), and for PC1 and PC2, 48% (not great, but ok for this dummy setup).

PC1 vs PC2 Biplot with clusters
![newplot (3)](https://user-images.githubusercontent.com/80417833/165811549-58332395-e06b-4f96-8a4f-5a384dedbefa.png)

## Clustering
Methods used:
* K-means clustering model of n clusters = 3
* Hierarchical model applied to features

Here are feature patterns of each cluster:

![newplot](https://user-images.githubusercontent.com/80417833/165811152-e27cb299-909a-481b-b8a0-3d6276b0e223.png)
![newplot (1)](https://user-images.githubusercontent.com/80417833/165811256-6820bb62-eae1-41b9-b953-7dee2e4cfb61.png)
![newplot (2)](https://user-images.githubusercontent.com/80417833/165811329-faa60eee-dea3-435a-bbc2-405d52c86da4.png)

## Outcomes
* 76% accuracy when comparing clusters to ground truth classification
* Acousticness best characterised songs that were 'calm, slow in tempo'
* Energy, loudness and tempo best characterised songs that were in the style of rock/metal
* Valence and danceability best characerised songs that were in the style of disco, 70s/80s pop
