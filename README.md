# number plate recognition


#Dependencies:

* [TensorFlow]
* OpenCV
* NumPy

http://matthewearl.github.io/2016/05/06/cnn-anpr/


Usage is as follows:
the sun webset : (http://groups.csail.mit.edu/vision/SUN/)

1. download the sun dataset(36GB) or just download the SUN2012(7.5gb)
(http://vision.princeton.edu/projects/2010/SUN/SUN397.tar.gz)
2. Extract ~3GB of background images from the [SUN database into `bgs/`. (`bgs/` must not already exist.)
----./extractbgs.py SUN2012.tar.gz

3.  Generate 1000 test set images in `train/`. (`train/` must not  already exist.)
---- ./generate.py 1000
    This step requires `UKNumberPlate.ttf`
    to be in the  `fonts/` directory, which can be   [downloaded here](http://www.dafont.com/uk-number-plate.font).

4. Train the model.
----- ./train.py
    the process will write the  weights to `weights.npz`.

5. Detect number plates in an image.
-----./detect.py test/test1.jpg weights.npz out.jpg



