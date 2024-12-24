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

7. GESTURE CONTROL

Implemented hand landmark model using OpenCV and Mediapipe, enabling real-time tracking and identification of hand movements.

Hand Landmark Model

After the palm detection over the whole image our subsequent hand landmark model performs precise keypoint localization of 21 3D hand-knuckle coordinates inside the detected hand regions via regression, that is direct coordinate prediction. The model learns a consistent internal hand pose representation and is robust even to partially visible hands and self-occlusions.

To obtain ground truth data, we have manually annotated ~30K real-world images with 21 3D coordinates, as shown below (we take Z-value from image depth map, if it exists per corresponding coordinate). To better cover the possible hand poses and provide additional supervision on the nature of hand geometry, we also render a high-quality synthetic hand model over various backgrounds and map it to the corresponding 3D coordinates.

Solution APIs

Configuration Options

Naming style and availability may differ slightly across platforms/languages.
STATIC_IMAGE_MODE
If set to false, the solution treats the input images as a video stream. It will try to detect hands in the first input images, and upon a successful detection further localizes the hand landmarks. In subsequent images, once all max_num_hands hands are detected and the corresponding hand landmarks are localized, it simply tracks those landmarks without invoking another detection until it loses track of any of the hands. This reduces latency and is ideal for processing video frames. If set to true, hand detection runs on every input image, ideal for processing a batch of static, possibly unrelated, images. Default to false.

MAX_NUM_HANDS
Maximum number of hands to detect. Default to 2.

MODEL_COMPLEXITY
Complexity of the hand landmark model: 0 or 1. Landmark accuracy as well as inference latency generally go up with the model complexity. Default to 1.

MIN_DETECTION_CONFIDENCE
Minimum confidence value ([0.0, 1.0]) from the hand detection model for the detection to be considered successful. Default to 0.5.

MIN_TRACKING_CONFIDENCE:
Minimum confidence value ([0.0, 1.0]) from the landmark-tracking model for the hand landmarks to be considered tracked successfully, or otherwise hand detection will be invoked automatically on the next input image. Setting it to a higher value can increase robustness of the solution, at the expense of a higher latency. Ignored if static_image_mode is true, where hand detection simply runs on every image. Default to 0.5.

![htm](https://github.com/user-attachments/assets/a222fb1d-3a03-49ce-bd3d-6259b283a618)


Source: MediaPipe Hands 


![photo-collage](https://github.com/user-attachments/assets/f572a665-a18a-4007-a043-d9384332f7e1)
