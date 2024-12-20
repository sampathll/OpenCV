# OpenCV
Computer vision is an exciting field of artificial intelligence that teaches computers to interpret and understand the visual world by using digital images from cameras and videos, and sophisticated deep learning models. By accurately identifying and classifying objects in the visual world, computer vision allows machines to make informed decisions and take appropriate actions based on what they "see".

OpenCV (Open Source Computer Vision Library) is a library of programming functions mainly aimed at real-time computer vision. Originally developed by Intel, it was later supported by Willow Garage then Itseez. The library is cross-platform and free for use under the open-source BSD license.

Here are the list of projects I did using opencv



1. ANGLE FINDER.

Created an Angle Finder. In that, I first define two lines using mouse clicks and then find the angle between theses lines using simple mathematics.

2. BRIGHTNESS AND VOLUME CONTROL.

Building a Volume Controller with OpenCV can be accomplished in just 3 simple steps:

Step 1. Detect Hand landmarks
Step 2. Calculate the distance between thumb tip and index finger tip.
Step 3. Map the distance of thumb tip and index finger tip with volume range. For my case, distance between thumb tip and index finger tip was within the range of 15 - 220 and the volume range was from -63.5 - 0.0 and brightness range of 0 - 100

3. OBJECTRON.

Objectron is a real-time 3D object detection solution for everyday objects. It detects objects in 2D images, and estimates their poses through a machine learning (ML) model. Currently supports Shoe, Chair, Cup & Camera.

4. DROWSINESS DETECTION

Driver drowsiness detection is a car safety technology which helps prevent accidents caused by the driver getting drowsy. Various studies have suggested that around 20% of all road accidents are fatigue-related, up to 50% on certain roads.

5. FACE ALIGNMENT

Face alignment is the task of identifying the geometric structure of faces in digital images, and attempting to obtain a canonical alignment of the face based on translation, scale, and rotation. Using Face Alignment we can get higher accuracy from our face recognition. As Face Alignment is like data normalization.
I have used pre-trained HOG + Linear SVM object detector specifically for the task of face detection.

6. EYE BLINK COUNT DETECTION

We can use eye blink count detector to check if eyes are blinking regularly or not to avoid the symptoms of Dry Eye. As eye blink is considered to be a suitable indicator for fatigue diagnostics. Drowsy state may be caused by lack of sleep, medication, drugs or driving continuously for long time period.

I have used pre-trained HOG + Linear SVM object detector specifically for the task of face detection. Download shape_predictor_68_face_landmarks.dat from here:- https://github.com/italojs/facial-landmarks-recognition/blob/master/shape_predictor_68_face_landmarks.dat
