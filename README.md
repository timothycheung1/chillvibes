# chillVibes

ChillVibes is a web application that plays music based on the facial expressions captured through the webcam. This is done using Azure facial recognition and Spotify Web API.

ChillVibes is split into mulpiple programs that perform different functions.

# moodQuantifier

moodQuantifier receives a screenshot from the webcam and returns a scoring chart of emotions portrayed by all the faces (if any) present in the image. This is done using Microsoft Azure Facial Recognition, which is capable of detecting the following emotions: emotion, anger, contempt, disgust, fear, happiness, neutral, sadness, suprise. moodQuantifer first sends the image (screenshot) through a Azure REST API. With scores returned from Azure, moodQuantifier then reads the emotion score of all the emotions for each face from the JSON and calculates a combined score for all the emotions, and returns an object with a score for each emotion.

# whatsTheVibe

whatsTheVibe receives an object containing 9 emotion scores: emotion, anger, contempt, disgust, fear, happiness, neutral, sadness, suprise, and determines what category of music fits the mood best. This is done using an algorithm that weighs each emotion score and produces a qualitative result: category of music.

# vibeSet

vibeSet receives a category of music and randomly chooses music to play based on playlists on Spotify corresponding to the category. This is done using Spotify Web API, which contain access to playlists that vibeSet can choose songs from. vibeSet can take in an integer in which the integer denotes the number of songs requested. vibeSet will then return the number of songs requested.

# Flow of Program

# Emotion to music category algorithm
