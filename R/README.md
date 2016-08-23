R data-sets:

Subsample of the Extended Yale Face Database B faces (cropped)
**************************************************************
Description: Grayscaled faces (8 bit [0-255]), 96x84 size. A few images of several different people
and 2410 total images. Each face image is flattened and stored as a column vector.

References: Lee, Kuang-Chih, Jeffrey Ho, and David J. Kriegman. "Acquiring linear subspaces for face recognition under variable lighting." IEEE Transactions on pattern analysis and machine intelligence 27, no. 5 (2005): 684-698.

Examples:
```R
utils::download.file('https://github.com/Benli11/data/raw/master/R/faces.RData', 'faces.RData')
load("faces.RData")

# Display 10th face
face <- matrix(rev(faces[,1]), nrow = 84, ncol = 96)
image(face, col = gray(0:255 / 255 ))
```


Highway
***********

Description: 176x144 grayscaled (8 bit [0-255]) surveillance video with 200 frames.
 Each frame is flattened, and stored as a column vector.

References: N. Goyette, P.-M. Jodoin, F. Porikli, J. Konrad, and P. Ishwar,
             changedetection.net: A new change detection benchmark dataset,
             in Proc. IEEE Workshop on Change Detection (CDW-2012) at CVPR-2012,
             Providence, RI, 16-21 Jun., 2012.
 
Source: http://changedetection.net/

Examples:
```R
utils::download.file('https://github.com/Benli11/data/raw/master/R/highway.RData', 'highway.RData')
load("highway.RData")

# Reshape and display the 100th frame:
frame <- matrix(highway[,100], ncol=144, nrow=176)
image(frame, col = gray((0:255)/255))
```
