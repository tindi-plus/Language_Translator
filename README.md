# Language_Translator
<img src="https://cdn.pixabay.com/photo/2013/05/12/09/36/globe-110775_1280.jpg" height="500"> *Image source: pixabay.com*

## Introduction
An application that translates speech from one language to another. The translation is done using Google Speech to Text Services.

## Installation
The program requires the speech_recognitionn library which can be installed by the following commnad on your windows command prompt: ***pip install SpeechRecognition***. Speech  More details about the library can be found on Pypi [here](https://pypi.org/project/SpeechRecognition/). 
TextBlob is another python natural language processing library that is required to run the program. It can be isntalled from Pypi with the following command: ***pip install textblob***. More details about textblob can be found [here](https://pypi.org/project/textblob/). The library pydub is an audio processing library. It can be installed with ***pip install pydub***. Google Text To Speech is is a python library for accessing Google's Translate API. The Google Text To Speech (gTTS) can be installed using pip: ***pip install gTTS***. To learn more about gTTS, visit [here](https://pypi.org/project/gTTS/).

## Description
The language translator is a program that translates one language to another. The program records an audio in one language and translates into another language that is specified by the user. The audio recording is done using speech_recognition's Microphone method. The audio is transcribed to text which is then translated using textblob. The translated text is then synthesized into speech using Google services. The synthesized speech is played for the user using pydub.
The function *record_audio* does the speech recording using speech_recognition's Microphone method. The recorded audio is returned in AudioData format.
The function *play_audio* plays an AudioData file using playdub. The function takes as an argument the audio file to be played.
The function *text_to_speech* takes as arguments the text file to convert to speech and the language to use. The function uses gTTS to synthesize the speech from the given text.
The function *speech_to_text* takes as argument the audio file to be transcribed to text. The function returns a text string of the transcription. Note that Google automatically detects the language of the speech hence there is no need to specify a language.
The sequence of steps of the program is as follows:
* The user is prompted to input the language code of the language they want to translate to.
* The user then speaks what he/she wants to translate, which is recorded by the program.
* The recorded speech is transcribed to text.
* The transcribed text is translated to the specified language using textblob
* The translated text is synthesized into speech.
* The speech is played by the program.

