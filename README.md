# Face detection, recognition and comparison

This is a mini - project for face detection, extraction, comparison, age and gender detection and weight, height and bmi estimation.

For face detection and extraction i use the algorithm in this repository https://github.com/Linzaer/Face-Track-Detect-Extract. It is based on a MultiTask Cascaded Convolutional neural network (MTCNN). The algorithm detects a face in a video, track it then outputs a list of tracked faces. One of the reasons for choosing this algorithms is its ability to detect side view and not only frontal faces.

We use two cameras which continuously sends videos extracted by (motioneye software) to two different directories. These videos are treated and faces are extracted and sent to two differents image directories with time label.

The face comparison function in Facenet algorithm (https://github.com/davidsandberg/facenet) is used. It computes  an image representation then compute the euclidian distance between two images. The decision function is fixed according to a distance threshold.

Another way to compare is extracting the fc6 (or another layer output) features in VGGFace algorithm and then compare it.

Note that facenet compare function is more powerful for our application than the one based on VGGFace's layer.

