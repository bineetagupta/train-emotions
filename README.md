# Train emotions

This is a repository dedicated for training machine learning models for voice files with emotions (angry, disgust, fear, happy, neutral, or surprised) from video files downloaded from Youtube.

![](https://media.giphy.com/media/3o6nUNpJn4VznakjKM/giphy.gif)

## Team members

Active members of the team working on this repo include:

* Bineeta Gupta (Arizona State University) 
* Luke Lyon (Boulder, CO)
* Anwar Akkari (Yale University) 
* Jim Schwoebel (Boston, MA) 
* Shivani Reddy (Clemson University) 

## Meeting times 

We plan to do slack updates every week 8 PM EST on Fridays. If we need to do a work session, we will arrange for that. 

## Goal / summary or prior models (how they were formed)  

Here are some goals to try to beat with demo projects. Below are some example files that classify various emotions with their accuracies, standard deviations, model types, and feature emebddings. It will give you a good idea on what to brush up on as you think about new embeddings for audio and text features for models. 

| Model Name	| Feature embedding | Accuracy	| Standard Deviation	| Modeltype| 
| ------------- | ------------- | ------------- | ------------- |------------- |
| disgust.pickle |	character, polarity, rhythm, spectral| 0.9775293015 |	0.009225004885	| random forest|
| surprise.pickle | character, polarity, onset, spectral, power |	0.8971036205 |	0.008219397678	| knn | 
| fear.pickle	| pos, polarity, spectral | 0.8406798246	| 0.003728070175	| knn |
| happy.pickle	| character, polarity, spectral, power | 0.68	| 0.03479685397	| hard voting |
| angry.pickle |	polarity, rhythm, spectral, power| 0.6548830038 |	0.04924646135	| gradient boosting |
| happy_sad.pickle	| power | 0.6543740573 |	0.01507843069 |	logistic regression |
| sad.pickle | character, polarity, rhythm, spectral, power |	0.6313155529	| 0.02186253158	| hard voting |
| happy_sad_neutral.pickle	| pos, spectral | 0.4698875525	| 0.02512849173	| logistic regression |
| all_emotions.pickle | character, pos, polarity, onset, rhythm, spectral |	0.2875083655	| 0.0358943377 |	knn | 

## Downloading the data

Make sure you have roughly 15 GB of free space on your hard disk.

Once you know you have this much space, you can download the dataset by clicking [this link](https://drive.google.com/open?id=1CA_9LR8q9npnmfCFcwtrdjB-kDN9g2QD). After you click on the link go to the top right corner of the page and click download (the icon with the down arrow). After this, the download should start. This could take a while based on your internet connection.

## Dataset summary / feature array 

The data is arranged in these folders: angry, disgust, fear, happpy, neutral, sad, surprise. Each wav file has a corresponding .json file with a transcript and features. The feature array in the .json file contains audio features (like mfcc coefficients and their deltas), as well as text features like part of speech tags. This is the standard mixed NeuroLex feature embedding. 

Feel free to make your own feature arrays to model the data; these are just here for guidance in case you don't feel comfortable making your own features and/or if you'd like to test this feature array vs. other feature arrays that you custom engineer. 

## Making new datasets 

If you would like to make a new dataset, please check out the sub-repository called [youtube_scrape](https://github.com/NeuroLexDiagnostics/train-emotions/tree/master/youtube_scrape). You can browse through existing links that we used for training videos in the past in the playlist folder of that repo. Instructions also are there for how to make new playlists. 

We can download the videos and extract features for you if you provide us the playlist URLs.

## Places to publish?? 

There are a few places we could publish this work. Here are the submission deadlines. 

| Conference  | Location |  Deadline to submit | Description | 
| ------------- | ------------- | ------------- | ------------- |
| [Interspeech](https://www.isca-speech.org/iscaweb/index.php/conferences/interspeech) | Austria | TBA | Crossroads of Speech and Language|

## References 
* [librosa](https://github.com/librosa/librosa)
* [spacy](https://spacy.io/)
* [numpy](http://www.numpy.org/)
* [scikit-learn](http://scikit-learn.org/stable/index.html)
* [keras](https://keras.io/)
