# Multiple-criminal-face-recognation-system-
Theory of OpenCV face recognizers::
Thanks to OpenCV, coding facial recognition is now easier than ever.
There are three easy steps to computer coding facial recognition, which are similar to the steps that our brains use for recognizing faces.
These steps are: 
Data Gathering: Gather face data (face images in this case) of the persons you want to identify. 
Train the Recognizer: Feed that face data and respective names of each face to the recognizer so that it can learn. 
Recognition: Feed new faces of that people and see if the face recognizer you just trained recognizes them.



The LBPH Face Recognizer Process
Take a 3×3 window and move it across one image. 
At each move (each local part of the picture), compare the pixel at the center, with its surrounding pixels.
Denote the neighbors with intensity value less than or equal to the center pixel by 1 and the rest by 0.
After you read these 0/1 values under the 3×3 window in a clockwise order, 
you will have a binary pattern like 11100011 that is local to a particular area of the picture. 
When you finish doing this on the whole image, you will have a list of local binary patterns.


In the end, you will have one histogram for each face in the training data set. 
That means that if there were 100 images in the training data set then LBPH will extract 100 histograms after 
training and store them for later recognition. Remember, 
the algorithm also keeps track of which histogram belongs to which person.

Later during recognition, the process is as follows:

   1.Feed a new image to the recognizer for face recognition.
   2.The recognizer generates a histogram for that new picture.
   3. It then compares that histogram with the histograms it already has.
   4. Finally, it finds the best match and returns the person label associated with that best match.


