# Voice-Assistant-with-Speech-Recognition
Voice assistant for working with data using queries.
---
#### Voice assistant is created using Speech Recognition and pyttsx3 packages. Let's go on with working principle of voice assistant.
Firstly, we are creating Recognizer using __sr.Recognizer()__ method. Each Recognizer instance has seven methods for recognizing speech from an audio source using various APIs. These are:

* recognize_bing(): Microsoft Bing Speech
* recognize_google(): Google Web Speech API
* recognize_google_cloud(): Google Cloud Speech - requires installation of the google-cloud-speech package
* recognize_houndify(): Houndify by SoundHound
* recognize_ibm(): IBM Speech to Text
* recognize_sphinx(): CMU Sphinx - requires installing PocketSphinx
* recognize_wit(): Wit.ai

I have used recognize_google method. For using this method we need an audio data to convert that audio data to text to print it or to use in wanted mission. So, to get that audio data I am using my microphone by the help of __sr.Microphone()__ command. Using __energy_threshold__, __adjust_for_ambient_noise__ and __pause_threshold__ I increased quality of audio which is recored with my microphone, then I am storing that record in variable **(said)**. In following step, we are converting that audio to text using **recognize_google** method which I have mention above with according to chosen language **(language='en-US')** and storing it in variable **(q)**. 
Secondly, we have **querying()** method which uses converted text to accomplish missions which is given with voice. As you see, first keyword is **entire data** which shows entire dataset, second is **describe** which applies **df.describe(include=all)** method, third is **show** or **features** which shows names of features in dataset, last one is **shut** or **down** which shuts down Voice Assistant. As an addition, I have chosen **Zira** voice because of waking up message. If you want you can change it to any of them. However, do not forget changing waking message too. I think you won't want to see David while telling "My name is Zira" :D .
