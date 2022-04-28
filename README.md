# Data Project using Spotipy music features 
* Used Spotipy to access the Spotify song library via its Web API
* Sourced Spotify audio feature data to create a dataset
* Preprocessed dataset by feature selection and scaling 
* Applied clustering and dimensionality reduction techniques to data

The objectives were to:
1. Apply clustering algorithms (K-Means and agglomerative) to the audio feature metadata of 300 songs equally representing 3 styles of music to see if it will successfully categorise them
2. Investigate the feature patterns of each cluster which would characterise a music genre/style for the songs clustered

Outcomes:
* 76% accuracy when comparing clusters to ground truth classification
* Acousticness best characterised songs that were 'calm, slow in tempo'
* Energy, loudness and tempo best characterised songs that were in the style of rock/metal
* Valence and danceability best characerised songs that were in the style of disco, 70s/80s pop
