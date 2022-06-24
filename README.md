# Pixabay - Multi-Task Music Dataset (MTMD)

## This is a dataset consisting of awesome royalty free music from [Pixbay Music](https://pixabay.com/music/).  
The music on their website contain tags of genre and mood.  Since a song may be a mixture of different genres and moods,
 the annotation will be multilabel containing all genres and moods of a music track.
 
 The whole dataset can be downloaded on [Pixabay MTMD](https://drive.google.com/drive/u/6/folders/1sTrv7DBm5vXniHf6dHsW4w5bG_4zh2NU)
 
 ## Analysis
 (The results can be obtained by running analysis.ipynb)
![All Genres](https://user-images.githubusercontent.com/61879226/175501523-4ff58c42-05d8-4997-ba7a-26523b0b09a3.png)
![All Moods](https://user-images.githubusercontent.com/61879226/175501572-650407aa-5ba3-4dab-a5ab-44efb0811118.png)

 The dataset now contains 374 music tracks, with 13 genres and 23 moods.  Some of the genres are related like 'Rock', 'HardRock', and 'Metal', but they don't necessarily
  appear together.  Also, some moods are related and need to be clustered.  Methods can be like **Tellegen-Watson-Clark model of mood** which cluster moods by positive/negative affection and high/low level:
  
![The-Tellegen-Watson-Clark-model-of-mood-figure-reproduced-from51](https://user-images.githubusercontent.com/61879226/175502893-a29c9294-c5b2-4ce4-ac43-c0361d3469f0.png)

## Feature Extraction

The timbre features can be helpful for multilabel mood prediction [ISMR2008](https://ismir2008.ismir.net/papers/ISMIR2008_275.pdf).
 - 13 MFCC + spectral centroid + spectral rolloff + spectral flux (**16 features** in total) in each frame
 - calculated the mean, standard deviation (std), mean standard deviation (mean std) and standard deviation
of standard deviation (std std) over all frames. This led to a total of **64 timbre features**.

In the last part of analysis.ipynb, I retrieved some timbre features using the method in the above study.  The computed features are along with the dataset.  

