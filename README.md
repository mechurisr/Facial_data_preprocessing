## Facial_data_preprocessing

The method used to create image dataset for facial emotion recognition project.  
(full project can be found here: https://github.com/mechurisr/finalProject)


This set of Jupiter Notebook codes collect image data from Google image using selenium, and identifies facial images to save them using Dlib and OpenCv.  
Also includes Facial Landmarking functions and guidelines to turn them into dataset.

### chromeCrawilingSel.pynb
* Requirements   
  * Chromedriver  
  * Selenium  
  * openCV (haarcascade_eye, haarcascade_frontalface_default)  
  * dlib (CMake build required)  
Either cv2 and dlib library can be used to collect facial images.(dlib tend to work slightly better but mere difference)  
Some not-face images(like pics or emojis) tend to be included in the collection as well, so will have to remove them manually...for now.  
can also resize images to certain pixels, and convert into gray images.


### FaceLandmark.ipynb
Uses dlib.get_frontal_face_detector and dlib.shape_predictor.  
Can place landmarks in multiple facial images with three shapes(line, dotted, and numbers).


### DataConcat.ipynb
Label images in a folder and dataframe it.  
convert the dataframe into a csv file.  
(For use in CNN models)
