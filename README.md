import speech_recognition as sr
from edgetts import EdgeTTS
import spacy

# Load spaCy's English language model
nlp = spacy.load("en_core_web_sm")

def recognize_speech():
    recognizer = sr.Recognizer()
    with sr.Microphone() as source:
        print("Listening...")
        recognizer.adjust_for_ambient_noise(source)
        audio = recognizer.listen(source)

   try:
    print("Recognizing...")
    text = recognizer.recognize_google(audio)
    print(f"You said: {text}")
    return text
except sr.UnknownValueError:
    print("Speech Recognition could not understand audio.")
    return ""
except sr.RequestError as e:
    print(f"Could not request results from Google Speech Recognition service; {e}")
    return "" try:
        print("Recognizing...")
        text = recognizer.recognize_google(audio)
        print(f"You said: {text}")
        return text
    except sr.UnknownValueError:
        print("Speech Recognition could not understand audio.")
        return ""
    except sr.RequestError as e:
        print(f"Could not request results from Google Speech Recognition service; {e}")
        return ""

def nlp_analysis(text):
    doc = nlp(text)
    return doc

def respond_to_user_intent(user_intent):
    if "exit" in user_intent:
        return "Goodbye!"
    elif "how are you" in user_intent:
        return "I'm doing well, thank you!"
    elif "tell a joke" in user_intent:
        return "Why don't scientists trust atoms? Because they make up everything!"
    elif "weather" in user_intent:
        return "I'm sorry, I don't have real-time weather information yet."
    else:
        return "I'm sorry, I didn't understand that. Can you please repeat?"

def speak(text):
    tts = EdgeTTS()
    tts.speak(text)

def ai_assistant():
    speak("Hello! How can I assist you today?")
    
   while True:
    user_input = recognize_speech().lower()

   iif "exit" in user_input:
speak("Goodbye!")
speak("Goodbye!")
breakiif "exit" in user_input:
    speak("Goodbye!")
    break

# Perform NLP analysis
doc = nlp_analysis(user_input)

# Extract user intent (for simplicity, we assume the first verb is the user's intent)
user_intent = next((token.lemma_ for token in doc if token.pos_ == "VERB"), "")

# Generate response based on user intent
response = respond_to_user_intent(user_intent)
speak(response) while True:
    user_input = recognize_speech().lower()

 if "exit" in user_input:
speak("Goodbye!")
breakif "exit" in user_input:
    speak("Goodbye!")
    break

# Perform NLP analysis
doc = nlp_analysis(user_input)

# Extract user intent (for simplicity, we assume the first verb is the user's intent)
user_intent = next((token.lemma_ for token in doc if token.pos_ == "VERB"), "")

# Generate response based on user intent
response = respond_to_user_intent(user_intent)
speak(response)f "exit" in user_input:
    speak("Goodbye!")
    break

# Perform NLP analysis
doc = nlp_analysis(user_input)

# Extract user intent (for simplicity, we assume the first verb is the user's intent)
user_intent = next((token.lemma_ for token in doc if token.pos_ == "VERB"), "")

# Generate response based on user intent
response = respond_to_user_intent(user_intent)
speak(response) while True:
    user_input = recognize_speech().lower()

  if "exit" in user_input:
        speak("Goodbye!")
        break

   # Perform NLP analysis
  doc = nlp_analysis(user_input)

  # Extract user intent (for simplicity, we assume the first verb is the user's intent)
  user_intent = next((token.lemma_ for token in doc if token.pos_ == "VERB"), "")

   # Generate response based on user intent
  response = respond_to_user_intent(user_intent)
    speak(response)if "exit" in user_input:
        speak("Goodbye!")
        break

   # Perform NLP analysis
  doc = nlp_analysis(user_input)

  # Extract user intent (for simplicity, we assume the first verb is the user's intent)
   user_intent = next((token.lemma_ for token in doc if token.pos_ == "VERB"), "")

   # Generate response based on user intent
  response = respond_to_user_intent(user_intent)
   speak(response)f "exit" in user_input:
        speak("Goodbye!")
        break

   # Perform NLP analysis
   doc = nlp_analysis(user_input)

   # Extract user intent (for simplicity, we assume the first verb is the user's intent)
  user_intent = next((token.lemma_ for token in doc if token.pos_ == "VERB"), "")

   # Generate response based on user intent
   response = respond_to_user_intent(user_intent)
    speak(response) while True:
        user_input = recognize_speech().lower()

  if "exit" in user_input:
            speak("Goodbye!")
            break

   # Perform NLP analysis
   doc = nlp_analysis(user_input)

   # Extract user intent (for simplicity, we assume the first verb is the user's intent)
   user_intent = next((token.lemma_ for token in doc if token.pos_ == "VERB"), "")

   # Generate response based on user intent
response = respond_to_user_intent(user_intent)
   speak(response)

if __name__ == "__main__":
    # Install the required libraries
    try:
        import edgetts
    except ImportError:
        print("Installing edge-tts...")
       try:
    print("Recognizing...")
    text = recognizer.recognize_google(audio)
    print(f"You said: {text}")
    return text
except sr.UnknownValueError:
    print("Speech Recognition could not understand audio.")
    return ""
except sr.RequestError as e:
    print(f"Could not request results from Google Speech Recognition service; {e}")
    return "" 
        try:
            from pip._internal import main as pipmain
        except ImportError:
            from pip import main as pipmain

   pipmain (["install", "edge-tts"])

 # Run the AI assistant
   ai_assistant() 
