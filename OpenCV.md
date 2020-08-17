# OpenCV #
https://docs.opencv.org/4.4.0/
https://docs.opencv.org/master/d0/de3/tutorial_py_intro.html

## History ##
OpenCV was started at Intel in 1999 by Gary Bradsky, and the first release came out in 2000. Vadim Pisarevsky joined Gary Bradsky to manage Intel's Russian software OpenCV team. In 2005, OpenCV was used on Stanley, the vehicle that won the 2005 DARPA Grand Challenge. Later, its active development continued under the support of Willow Garage (also see ROS) with Gary Bradsky and Vadim Pisarevsky leading the project (later Itseez Inc.).  In August 2012, the responsibility for further development and support for OpenCV was assumed by an independent, not-for-profit organization, OpenCV.org. On May 25, 2016, Intel acquired Itseez Inc., "an expert in Computer Vision algorithms and implementations for embedded and specialized hardware."
OpenCV now supports a multitude of algorithms related to Computer Vision and Machine Learning and is expanding day by day.

OpenCV supports a wide variety of programming languages such as C++, Python, Java, etc., and is available on different platforms including Windows, Linux, OS X, Android, and iOS. Interfaces for high-speed GPU operations based on CUDA and OpenCL are also under active development.

OpenCV-Python is the Python API for OpenCV, combining the best qualities of the OpenCV C++ API and the Python language.

OpenCV is released under a BSD license and hence it's free for both academic and commercial use. It has C++, C, Python and Java interfaces and supports Windows, Linux, MacOS, iOS and Android. OpenCV was designed for computational efficiency and with a strong focus on real-time applications. Written in optimized C/C++, the library can take advantage of multi-core processing. Enabled with OpenCL, it can take advantage of the hardware acceleration of the underlying heterogeneous compute platform.

Joseph Howse and Joe Minichino: Learning OpenCV 4 Computer Vision with Python 3, Packt Publishing
Ashwin Pajankar: Raspberry Pi Computer Vision Programming, Packt Publishing

## Introduction ##
OpenCV has a modular structure, which means that the package includes several shared or static libraries. The following modules are available:
- Core functionality (core) - a compact module defining basic data structures, including the dense multi-dimensional array Mat and basic functions used by all other modules.
- Image Processing (imgproc) - an image processing module that includes linear and non-linear image filtering, geometrical image transformations (resize, affine and perspective warping, generic table-based remapping), color space conversion, histograms, and so on.
- Video Analysis (video) - a video analysis module that includes motion estimation, background subtraction, and object tracking algorithms.
- Camera Calibration and 3D Reconstruction (calib3d) - basic multiple-view geometry algorithms, single and stereo camera calibration, object pose estimation, stereo correspondence algorithms, and elements of 3D reconstruction.
- 2D Features Framework (features2d) - salient feature detectors, descriptors, and descriptor matchers.
- Object Detection (objdetect) - detection of objects and instances of the predefined classes (for example, faces, eyes, mugs, people, cars, and so on).
- High-level GUI (highgui) - an easy-to-use interface to simple UI capabilities.
- Video I/O (videoio) - an easy-to-use interface to video capturing and video codecs.
... some other helper modules, such as FLANN and Google test wrappers, Python bindings, and others.

## OpenCV-Python ##
OpenCV-Python is a library of Python bindings designed to solve computer vision problems.

Python is a general purpose programming language started by Guido van Rossum that became very popular very quickly, mainly because of its simplicity and code readability. It enables the programmer to express ideas in fewer lines of code without reducing readability.

Compared to languages like C/C++, Python is slower. That said, Python can be easily extended with C/C++, which allows us to write computationally intensive code in C/C++ and create Python wrappers that can be used as Python modules. This gives us two advantages: first, the code is as fast as the original C/C++ code (since it is the actual C++ code working in background) and second, it easier to code in Python than C/C++. OpenCV-Python is a Python wrapper for the original OpenCV C++ implementation.

OpenCV-Python makes use of Numpy, which is a highly optimized library for numerical operations with a MATLAB-style syntax. All the OpenCV array structures are converted to and from Numpy arrays. This also makes it easier to integrate with other libraries that use Numpy such as SciPy and Matplotlib.

pip install opencv-python

## Learning to use OpenCV ##
Learn OpenCV in 3 hours with Python
https://www.youtube.com/watch?v=WQeoO7MI0Bs

Ashwin Pajankar: Raspberry Pi Computer Vision Programming, 2nd Edition, Packt Publishing

## RasPi Camera Modules ##

+-------------------+---------------------+---------------------+
|                   | High Quality Camera |  Camera Module v2   |
+-------------------+---------------------+---------------------+
| Sensor            |   Sony IMX477       |    Sony IMX219      |
| Sensor resolution |  4056 x 3040 px     |   3280 x 2464 px    |
|                   |      12.33 MP       |        8 MP         |
| Sensor area       |  7.857 x 7.857 mm   |    3.69 x 2.81 mm   |
| Image modes       | 4056 x 3040, 60 fps | 1920 x 1080, 30 fps |
|                   |   2028 x 1520       | 1280 x  720, 60 fps |
|                   | 2028 x 1080, 240 fps|  640 x  480, 90 fps |
|                   |   1012 x  760       |                     |
+-------------------+---------------------+---------------------+
| Price             |   about EUR 55      |     about EUR 30    |
+-------------------+---------------------+---------------------+

## Terminology ##

## Interesting Links ##

CodeCentric: Einführung in CV mit OpenCV und Python
https://blog.codecentric.de/2017/06/einfuehrung-in-computer-vision-mit-opencv-und-python/

YOLO: Real-Time Object Detection
https://pjreddie.com/darknet/yolo/
Convolutional Neural Network (CNN), das in Echtzeit (auf entsprechender Hardware) verschiedenste Klassen von Objekten erkennen kann

Mahotas: Computer Vision in Python
https://mahotas.readthedocs.io/en/latest/

## OpenCV-Python Tutorial ##
https://docs.opencv.org/4.4.0/d6/d00/tutorial_py_root.html

## OpenCV 4 on Ubuntu 20.04 ##
- how to install OpenCV 4 on Ubuntu 20.04 using a virtual machine


## Raspi CV Programming ##
Work environment: Raspi 4, 4 GB RAM, Camera Module v2, Raspberry Pi OS

## Advanced Computer Vision with Tensorflow 2.x ##
https://www.packtpub.com/data/advanced-computer-vision-with-tensorflow-2-x
Computer vision allows machines to gain human-level understanding to visualize, process, and analyze images and videos. This book focuses on using TensorFlow to help you learn advanced computer vision tasks such as image acquisition, processing, and analysis. You'll start with the key principles of computer vision and deep learning to build a solid foundation, before covering neural network architectures and understanding how they work rather than using them as a black box. Next, you'll explore architectures such as VGG, ResNet, Inception, R-CNN, SSD, YOLO, and MobileNet. As you advance, you'll learn to use visual search methods using transfer learning. You'll also cover advanced computer vision concepts such as semantic segmentation, image inpainting with GAN's, object tracking, video segmentation, and action recognition. Later, the book focuses on how machine learning and deep learning concepts can be used to perform tasks such as edge detection and face recognition. You'll then discover how to develop powerful neural network models on your PC and on various cloud platforms. Finally, you'll learn to perform model optimization methods to deploy models on edge devices for real-time inference. By the end of this book, you'll have a solid understanding of computer vision and be able to confidently develop models to automate tasks.

