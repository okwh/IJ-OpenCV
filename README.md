IJ-OpenCV is a Java library that allows the communication of ImageJ - a software for image analysis that is widely employed in life sciences - and OpenCV - a well-known computer vision library.

There are several benefits provided by the communication of ImageJ and OpenCV. From the ImageJ perspective, this tool is enhanced with several computer vision and machine learning algorithms, avoiding the re-implementation of methods and the connection with several external libraries. From the OpenCV point of view, this library is improved with a simple-to-use GUI and with the functionality to manage regions of interest.

This new version of IJ-OpenCV has been built on top of SciJava Common using SciJava converters.

IJ-OpenCV is free to use and licensed under the license GNU GPL 3.0.

### Citation
If you use IJ-OpenCV for your research please cite :  
* Domínguez, César, Jónathan Heras, and Vico Pascual. "IJ-OpenCV: Combining ImageJ and OpenCV for processing images in biomedicine." Computers in biology and medicine 84 (2017): 189-194.

### Installation

#### - In Fiji
In Fiji, the library and plugins can be installed by simply ticking the IJ-OpenCV update site in your Fiji updater (_Help>Update>Manage Update sites_).

#### - With Maven
You can download and install the IJ-OpenCV library using maven; namely, including the following dependency in your pom.xml file:
```xml
      <repositories>
        <repository>
            <id>ossrh</id>
            <url>https://oss.sonatype.org/content/repositories/snapshots</url>
        </repository>
      </repositories>
      ...
      <dependencies>
        <dependency>
            <groupId>io.github.joheras</groupId>
            <artifactId>IJ-OpenCV</artifactId>
            <version>1.2.1-SNAPSHOT</version>
        </dependency>
      ...
      </dependencies>
```

#### - Manual installation (ex: ImageJ)
The recommended installation procedure to include IJ-OpenCV in your project is the use of maven, but you can also directly download the IJ-OpenCV 1.0 binary archive [IJ-OpenCV-1.0.jar](http://search.maven.org/remotecontent?filepath=io/github/joheras/IJ-OpenCV/1.0/IJ-OpenCV-1.0.jar). You will also need to install the binary files of [JavaCV](https://github.com/bytedeco/javacv).  
In order to execute the FaceDetection plugin it is necessary to download the following [file](https://github.com/joheras/IJ-OpenCV/blob/master/utils/haarcascade_frontalface_alt.xml) and copy it to a new subfolder `lib` in ImageJ installation folder.

#### - Test images
You can download several images to test the plugins at the following [link](https://github.com/joheras/IJ-OpenCV/blob/master/utils/images.zip).

### System requirements
IJ-OpenCV requires that ImageJ works with Java 8.

### Documentation
Have a look at the [wiki](https://github.com/joheras/IJ-OpenCV/wiki) section for some help about how to use IJ-OpenCV in your own scripts.  
Or at the [IJ-OpenCV API documentation](https://joheras.github.io/IJ-OpenCV/) and related [OpenCV API documentation](https://www.javadoc.io/doc/org.bytedeco.javacpp-presets/opencv/3.4.2-1.4.2/).

### Source files
The source files of the IJ-OpenCV library are available at the following [link](https://github.com/joheras/IJ-OpenCV).

### List of IJ-OpenCV plugins
The source code of the following plugins can be found in the examples folder. 
* Adaptive threshold: Given an image, it applies either the adaptive Gaussian threshold or the adaptive mean threshold. [OpenCV link to the topic](http://docs.opencv.org/2.4/modules/imgproc/doc/miscellaneous_transformations.html?highlight=adaptive%20threshold#adaptivethreshold).
* BGR histogram comparison: Given a stack of images, it compares the images using the BGR histogram and employing different measures . [OpenCV link to the topic](http://docs.opencv.org/2.4/doc/tutorials/imgproc/histograms/histogram_calculation/histogram_calculation.html?highlight=histogram).
* Black hat: Given a grayscale image, it returns such an image after applying the black hat morphological operation. [OpenCV link to the topic](http://docs.opencv.org/2.4/doc/tutorials/imgproc/opening_closing_hats/opening_closing_hats.html?highlight=black%20hat#black-hat).
* Canny edge detection: Given an image, it detects its using the Canny edge detection algorithm. [OpenCV link to the topic](http://docs.opencv.org/2.4/modules/imgproc/doc/feature_detection.html?highlight=canny%20edge%20detection#void%20Canny%28InputArray%20image,%20OutputArray%20edges,%20double%20threshold1,%20double%20threshold2,%20int%20apertureSize,%20bool%20L2gradient%29).
* Convex hull from polygon: Given a polygonal selection, it returns its convex hull . [OpenCV link to the topic](http://docs.opencv.org/2.4/doc/tutorials/imgproc/shapedescriptors/hull/hull.html?highlight=convex%20hull).
* Detect circles: Given an image, it detects the circles of such an image using the Hough Circle transform. [OpenCV link to the topic](http://docs.opencv.org/2.4/doc/tutorials/imgproc/imgtrans/hough_circle/hough_circle.html?highlight=hough%20circles).
* Face detection: Given an image, it detects the faces of the image. With ImageJ, it is necessary to download the following [file](https://github.com/joheras/IJ-OpenCV/blob/master/utils/haarcascade_frontalface_alt.xml) and copy it to a new subfolder `lib` in ImageJ installation folder. [OpenCV link to the topic](http://docs.opencv.org/2.4/modules/contrib/doc/facerec/facerec_tutorial.html).
* Find contours: Given an image, it detects the contours of the objects of such an image. [OpenCV link to the topic](http://docs.opencv.org/2.4/doc/tutorials/imgproc/shapedescriptors/find_contours/find_contours.html?highlight=find%20contours).
* High dynamic range imaging: Given a stack of images, it creates a high dynamic range image using the exposure fusion. [OpenCV link to the topic](http://docs.opencv.org/3.0-beta/doc/tutorials/photo/hdr_imaging/hdr_imaging.html).
* Hough Lines: Given an image, it computes the lines of the image using the Hough transform. [OpenCV link to the topic](http://docs.opencv.org/2.4/doc/tutorials/imgproc/imgtrans/hough_lines/hough_lines.html?highlight=hough%20lines).
* HSV histogram comparison: Given a stack of images, it compares the images using the HSV histogram and employing different measures . [OpenCV link to the topic](http://docs.opencv.org/2.4/doc/tutorials/imgproc/histograms/histogram_calculation/histogram_calculation.html?highlight=histogram).
* Keypoint detector: Given an image, it detects its keypoints using different algorithms. [OpenCV link to the topic](http://docs.opencv.org/2.4/modules/features2d/doc/common_interfaces_of_feature_detectors.html?highlight=keypoint).
* Kmeans clustering: Given a stack of images, it groups them using the BGR histogram as features and the Kmeans clustering algorithm. [OpenCV link to the topic](http://docs.opencv.org/2.4/modules/core/doc/clustering.html?highlight=kmeans).
* Non local means denoising: Given an image, it applies non local means denoising. [OpenCV link to the topic](http://docs.opencv.org/2.4/modules/photo/doc/denoising.html).
* RotatedRect from a polygon ROI: Given a polygonal selection, it returns the associated rotated rectangle. [OpenCV link to the topic](http://docs.opencv.org/2.4/modules/core/doc/basic_structures.html?highlight=rotated%20rect#RotatedRect).
* Stitching: Given an array of images, it stitches them creating a panoramic view. [OpenCV link to the topic](http://docs.opencv.org/2.4/modules/stitching/doc/introduction.html?highlight=stitching).
* Template Matching: Given an image, and a selection (template) in that image, it finds all the other regions of the image that match with the template. [OpenCV link to the topic](http://docs.opencv.org/2.4/doc/tutorials/imgproc/histograms/template_matching/template_matching.html?highlight=template%20matching).
* White Hat: Given a grayscale image, it returns such an image after applying the white hat morphological operation. [OpenCV link to the topic](http://docs.opencv.org/2.4/doc/tutorials/imgproc/opening_closing_hats/opening_closing_hats.html?highlight=black%20hat#top-hat).

### Videos
We include several videos showing how the plugins developed with the IJ-OpenCV library work.

#### Video 1
This first video shows how the "adaptive thresholding", "BGR Histogram Comparison" and "HSV Histogram comparison" plugins work.

[![Everything Is AWESOME](http://www.mailpoet.com/wp-content/uploads/2012/01/wysija-youtube-color-player.png)](https://www.youtube.com/watch?v=ERoqTnUOayA)

#### Video 2
This second video shows how the following plugins work:
* BlackHat and White Hat morphological operators
* Canny edge detection
* Convex hull from polygon ROI
* Circle detection
* Measure oxidation
* Face detection
* Find Contours
* High Dynamic Range Imaging

[![Everything Is AWESOME](http://www.mailpoet.com/wp-content/uploads/2012/01/wysija-youtube-color-player.png)](https://www.youtube.com/watch?v=BMGhKQZWhs8)

### Issues
To report bug and/or issues, you can open a [github issue](https://github.com/joheras/IJ-OpenCV/issues) provided you have a GitHub account (free).  
You can also create a topic on the [central image processing forum](forum.image.sc), and tagging @joheras and/or @LThomas. 

### Contact
Jónathan Heras (joheras@gmail.com)
