<h1 align="center">SAPA Project by C242-PS212 Team </h1>
<p align="center">"Sign Language Personal Assistant"</p>

# Backgrounder
Indonesia has over 923,941 individuals who are deaf or hard of hearing, often facing communication chalenges, especialy with those who do not understand sign language. Our team's experience interacting with a deaf food vendor highlighted the communication barriers caused by a lack of understanding of sign language. This issue demonstrates the need for a solution to bridge the communication gap between both parties. Our project aims to develop a video processing application that can recognize sign language and translate it into Indonesian, facilitating interaction between the deaf community and the general public.

The application we developed, SAPA (Sign Language Personal Assistant), has two main features: sign language recognition and translation into Indonesian. Using advanced video processing technology, the app captures and interprets sign language gestures in real-time and translates them into Indonesian. With a user-friendly interface, SAPA is designed to facilitate communication between deaf individuals and those who do not understand sign language, ensuring accessibility for the entire community. SAPA is expected to improve interaction and understanding between the deaf community and the general public.Detailed works on each learning path include:
1. Machine Learning: building models with TensorFlow lite and TensorFlow. Js, using data pipeline to serve the models, and preprocess the data using Missing Values Imputation.
2. Mobile Development: Deployment of TensorFlow lite and creation of both a user and an admin app. The application has a real-time connection using Firebase and a mechanism to adatabufferincaseaninternet connection is unavailable.
3. Cloud Computing: Implementing a REST API with Node.js for profile management and user authentication using Firebase Authentication. User data is stored in Firestore, and the app is deployed on Cloud Run. Google Cloud Storage is used for storing ML models, with access controled through Service Accounts.

---

# Machine Learning Track's Scope
## Methodology
1. Data Collection: Used OpenCV to access the camera and process video frames (e.g., RGB to BGR conversion). The sign language recognized is Bisindo (Bahasa Isyarat Indonesia).
2. Landmark Detection: Employed MediaPipe Holistic to detect and record coordinates of the face, body pose, left hand, and right hand.
3. Feature Extraction: Detected landmarks were flattened into 1D arrays and saved as .npy files. Missing landmarks were filled with zeros.
4. Preprocessing: Applied label mapping and split the data into training and testing sets.
5. Model Development: A Bi-LSTM model was used to recognize gestures. Unlike standard LSTM (which works one way and fits static gestures), Bi-LSTM reads sequences in both directions, making it more effective for dynamic sign language recognition.

## Result and Evaluation
The system is capable of translating five gestures: "A", "eat", "play", "who", and "why". The developed model achieved an overall accuracy of 87.5%.

Due to hardware limitations, the model could only be trained to recognize five gestures. Adding more caused training timeouts or memory errors. We balanced model complexity to avoid overfitting/underfitting using a 128–64–32 structure with dropout adjustments. Limited and less diverse data also affected accuracy.

---

# Important Links
- Screenshots/demo video: https://drive.google.com/drive/folders/1x_FMPNB8TomKzzd0Uz72-4pXqSN2UuNg?usp=sharing
- Dataset Link: https://drive.google.com/drive/folders/1u4h5czEuaMrKDWpd5Kp5Ao6ki-CP3HFC?usp=sharing
- Deployed Link: https://drive.google.com/drive/folders/1-ri5tBwhzNgKsccmprZW-LdpY9ox-Qe8?usp=sharing
- Video presentation link: https://drive.google.com/drive/folders/1IJPRFJyD43nHG69vUWdlAJofKP-hnhMg?usp=sharing
- Slide presentation link: https://drive.google.com/file/d/1UEhY2rJkdAggxJStS1lv6u3ts2AYpSJn/view?usp=sharing
