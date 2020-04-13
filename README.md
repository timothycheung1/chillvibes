# chillVibes

ChillVibes is a web application that plays music based on the facial expressions captured through the webcam. This is done using AWS Amazon Rekognition and Spotify Web API.

ChillVibes is split into mulpiple programs that perform different functions.

# moodQuantifier

moodQuantifier receives a screenshot from the webcam and returns emotions present in the image, along with each level of confidence. This is done using Amazon Rekognition, which is capable of detecting the following emotions: happy, sad, angry, confused, disgusted, surprised, calm, unknown, fear. moodQuantifer first sends the image (screenshot) through Amazon Rekognition API. With scores returned, moodQuantifier then combines all scores and returns a score for each emotion.

# whatsTheVibe

whatsTheVibe receives an object containing 9 emotion scores: happy, sad, angry, confused, disgusted, surprised, calm, unknown, fear, and determines what category of music fits the mood best. This is done using an algorithm that weighs each emotion score and produces a qualitative result: category of music.

# vibeSet

vibeSet receives a category of music and randomly chooses music to play based on playlists on Spotify corresponding to the category. This is done using Spotify Web API, which contain access to playlists that vibeSet can choose songs from. vibeSet can take in an integer in which the integer denotes the number of songs requested. vibeSet will then return the number of songs requested.

# Flow of Program

# Emotion to music category algorithm
