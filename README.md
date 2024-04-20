# Speech Recognition
Speech recognition is a fascinating field of artificial intelligence that has gained significant popularity in recent years. It enables computers to understand and interpret human speech, making it possible to build applications like voice assistants, and much more. Python, with its vast ecosystem of libraries and tools, is an excellent choice for working on speech recognition projects.

Speech recognition primarily focuses on converting spoken language into written text or computer commands. It is concerned with understanding the words and phrases spoken by a user and transcribing them into text.
Speech recognition is commonly used for tasks like transcription services, voice assistants (e.g., Siri, Google Assistant), and voice command systems where the intent is to understand what the user is saying and convert it into a usable format.

![image](https://github.com/Alphawarrior21/SpeechRecog/assets/30016067/aaef7711-1608-411d-99d9-b15bbca6139e)

# Popular Python Libraries for Speech Recognition
Python offers several powerful libraries and tools for working with speech recognition. Some of the most widely used ones include:

**SpeechRecognition, PyDub, pocketsphinx, deepspeech, Google Cloud Speech-to-Text, Watson Developer Cloud (IBM Watson), Microsoft Azure Cognitive Services Speech SDK**

# Why this SpeechRecognition package?

There are multiple packages available but I prefer SpeechRecognition because it’s very user friendly, flexible and easy to integrate. SpeechRecognition offers multiple functionality’s like —
- Convert audio file to text
- Convert audio from microphone to text
- Deal with noise in audio

SpeechRecognition package basically a wrapper for several popular speech APIs, it includes the Google Web Speech API, openai whisper api and many more which comes with a default API key already integrated into the SpeechRecognition package. This means you can try without signing up for a service. This level of flexibility and easy to integration make it better choice for python projects.

# Building a Simple Application using SpeechRecognition
The SpeechRecognition library, also known as SpeechRecognition or speech_recognition, is a Python library that provides a simple and user-friendly interface to work with various ASR engines, such as Google Web Speech API, CMU Sphinx, and more. It supports multiple audio input sources and is an excellent choice to start.

First, make sure you have python and pip installed:
# To install SpeechRecognition package
pip install SpeechRecognition

As per my experience recognize_whisper() gives the best result, if you want to try this you will require some other packages like:

pip install numpy

pip install soundfile

pip install torch

pip install git+https://github.com/openai/whisper.git


**Code Snippet**

    import speech_recognition as sr

    #Initialize the recognizer
    recognizer = sr.Recognizer()
    #Load an audio file
    audio_file = "sample_audio.wav"

    #Open the audio file
    with sr.AudioFile(audio_file) as source:
    #Record the audio data
    audio_data = recognizer.record(source)
    try:
        # Recognize the speech
        text = recognizer.recognize_google(audio_data)
        print("Recognized speech: ", text)
    except sr.UnknownValueError:
        print("Speech recognition could not understand the audio.")
    except sr.RequestError as e:
        print(f"Could not request results from service; {e}")

**Other recognize models in speech_recognition**

recognizer.recognize_google(),
recognizer.recognize_tensorflow(),
recognizer.recognize_whisper(),
recognizer.recognize_sphinx(), 
recognizer.recognize_google_cloud(), 
recognizer.recognize_wit(), 
recognizer.recognize_azure(), 
recognizer.recognize_bing(), 
recognizer.recognize_lex(), 
recognizer.recognize_houndify(), 
recognizer.recognize_amazon(), 
recognizer.recognize_assemblyai(), 
recognizer.recognize_ibm()



**Where can we use Speech recognition?**
Speech recognition in Python has a wide range of practical applications, including:

Voice Assistants: Building your own voice-controlled assistant like Siri or Alexa.
Transcription Services: Automatically converting spoken content into text, useful for transcription services or closed captioning.
Voice Commands: Creating applications that respond to voice commands, such as home automation systems.
Language Learning: Developing tools for language learners to practice pronunciation.
Accessibility: Enhancing accessibility for individuals with disabilities by enabling them to interact with computers and devices through speech.
Customer Support: Implementing speech recognition for automated customer support and interactive voice response (IVR) systems.
