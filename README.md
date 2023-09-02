Here's a README for our code:

# Advanced Face Recognition System using Realtime Database

This project is an advanced face recognition system that uses a realtime database to store and retrieve information about recognized faces. The system consists of two parts: an encode generator and a main file.

The encode generator uses the `face_recognition` library to encode faces from images stored in a local folder. The encoded faces are then stored in a database along with the corresponding student IDs.

The main file uses the `face_recognition` library to detect and encode faces in real-time video captured from a webcam. The encoded faces are then compared with known faces stored in the database to identify the person.

## Dependencies

This project requires the following libraries:
- `cv2`
- `face_recognition`
- `pickle`
- `os`
- `firebase_admin`
- `bbox`
- `numpy`
- `cvzone`

Make sure to install these dependencies before running the code.

## Setup

Before running the code, you need to set up a Firebase project and download the service account key JSON file. Replace the path to the JSON file in the following line of code:
```python
cred = credentials.Certificate("serviceAccountKey.json")
```

You also need to update the database URL and storage bucket URL with your own Firebase project information:
```python
firebase_admin.initialize_app(cred,{
    'databaseURL':"https://faceattendancerealtime-195ab-default-rtdb.firebaseio.com/",
    'storageBucket': "faceattendancerealtime-195ab.appspot.com"
})
```

## Usage

First, run the encode generator to encode faces from images stored in a local folder and store them in the database. Then, run the main file to start capturing video from your webcam and display it on the screen. When a face is detected, the program will attempt to recognize it by comparing it with known faces stored in the database. If a match is found, the program will display information about the recognized person on the screen.

# for database set up

# Student Database using Firebase

This project is a simple student database that uses Firebase to store and retrieve information about students. The system uses the `firebase_admin` library to interact with a Firebase realtime database.

## Dependencies

This project requires the following libraries:
- `firebase_admin`
- `datetime`

Make sure to install these dependencies before running the code.

## Setup

Before running the code, you need to set up a Firebase project and download the service account key JSON file. Replace the path to the JSON file in the following line of code:
```python
cred = credentials.Certificate("serviceAccountKey.json")
```

You also need to update the database URL with your own Firebase project information:
```python
firebase_admin.initialize_app(cred,{
    'databaseURL':"https://faceattendancerealtime-195ab-default-rtdb.firebaseio.com/"
})
```



## Usage

To run the code, simply execute it using a Python interpreter. The program will add student data to the database under the `Students` reference. Each student is represented by a unique key and their information is stored as a dictionary of key-value pairs.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
