## opencv-python

# !pip install opencv-python
```py
import cv2
cap = cv2.VideoCapture(0)
if not cap.isOpened():
    print("Error: Could not access the camera.")
    exit()
ret, frame = cap.read()
if ret:
    cv2.imwrite("captured_image.jpg", frame)
    print("Image saved as captured_image.jpg")
else:
    print("Error: Could not capture image.")
cap.release()
cv2.destroyAllWindows()
```

## pyautogui
# !pip install pyautogui
```py
import pyautogui

screenshot = pyautogui.screenshot()

screenshot.save("screenshot.png")

print("Screenshot saved as screenshot.png")
```

## SpeechRecognition
# !pip install SpeechRecognition
# !pip install pyaudio

```py
import speech_recognition as sr

recognizer = sr.Recognizer()

with sr.Microphone() as source:
    print("Say something...")
    audio = recognizer.listen(source)

try:
    text = recognizer.recognize_google(audio)
    print("You said: " + text)
except sr.UnknownValueError:
    print("Sorry, I could not understand the audio")
except sr.RequestError as e:
    print(f"Could not request results from Google Speech Recognition service; {e}")

```
